# GFG Problems Scraper

A Node.js script to scrape GeeksforGeeks (GFG) question data from the practice API. It extracts problem name, difficulty, accuracy, tags (both company and topic), and problem URLs, and saves the data in a structured CSV file for analysis and reference.

## Features

- Fetches data for **all 151 pages** from the GeeksforGeeks practice API.
- Extracts the following information for each problem:
  - **Problem Name**
  - **Difficulty**
  - **Accuracy**
  - **Topic Tags** (company tags are excluded)
  - **Problem URL**
- Saves the extracted data in a CSV file: `all_problems_with_tags_and_accuracy.csv`.

## Example Output

The generated CSV file contains the following columns:

| ID   | Problem Name                   | Difficulty | Accuracy | Topic Tags                                       | URL                                                   |
|------|--------------------------------|------------|----------|--------------------------------------------------|-------------------------------------------------------|
| 1    | Do - While Loop               | Easy       | 77.02%   |                                                  | https://www.geeksforgeeks.org/problems/do-while-loop/1 |
| 2    | Longest subsequence with difference | Medium | 43.43%   | Hash, Arrays, Algorithms                         | https://www.geeksforgeeks.org/problems/longest-subsequence-with-difference |
| 3    | Indexes of Subarray Sum       | Medium     | 16.5%    | Algorithms, Arrays, Data Structures, prefix-sum  | https://www.geeksforgeeks.org/problems/subarray-with-given-sum-1587115621 |

## Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- Basic knowledge of running Node.js scripts.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/gfg-problems-scraper.git
   cd gfg-problems-scraper
2. Install dependencies:
     ```bash
       npm install
Usage
Run the script:
    ```bash
      
      node index.js
        
Once the script completes, the output file all_problems_with_tags_and_accuracy.csv will be created in the project directory.

Customization
Pagination: The script fetches all 151 pages by default. You can adjust the MAX_PAGES constant in the script to limit the number of pages fetched.

Output File Name: The output file is named all_problems_with_tags_and_accuracy.csv by default. You can change the file name in the saveToCSV function.

Error Handling
If the script encounters an error (e.g., network issues), it will log the error message and continue to the next page.
Any problematic pages will be skipped, ensuring the script doesn't break.
Contributing
Contributions are welcome! If you have ideas for improving the script, feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
