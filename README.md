# Exact Word Counter

A high-fidelity, client-side web application for precise text analysis in real-time. This tool is a Progressive Web App (PWA) with full offline functionality.

## Usage

1. Open `index.html` in your browser.
2. Type or paste text into the text area.
3. The statistics will update in real-time and your text and preferences are saved for later visits.
4. Use the controls to change counting mode, configuration, or switch to dark mode.
5. Click **Copy Stats** to copy the current metrics to your clipboard.
6. Click **Download Stats** to export metrics and top words as a JSON file.
7. Click **Share Stats** to share your metrics using the Web Share API (falls back to copying).
8. Click **Clear Text** to reset the editor and stats.

The statistics include Flesch Reading Ease and grade-level scores to help evaluate text difficulty.

## Testing Checklist

The application's output must **exactly** match the expected values when configured as specified.

*   **Test Configuration:**
    *   **Mode:** `Smart`
    *   **Count numbers:** `ON`
    *   **Treat hyphenated terms as one word:** `ON`

*   **Test Input Text:**
    ```
    This state-of-the-art PWA is test #1. Don't you agree? It works in 日本語 too… What a result!
    ```

*   **Expected Output:**

| Metric                  | Expected Value |
| ----------------------- | :------------: |
| Words                   |       20       |
| Sentences               |       4        |
| Lines                   |       1        |
| **Top 5 Words**         |                |
| 1. `this`               |       2        |
| 2. `state-of-the-art`   |       1        |
| 3. `pwa`                |       1        |
| 4. `is`                 |       1        |
| 5. `test`               |       1        |
