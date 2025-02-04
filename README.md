# Indeed-data-scraping-and-visualization
![image](https://github.com/user-attachments/assets/6209e42c-da3e-4363-8404-8d719d1abdf2)
[Tableau](https://public.tableau.com/app/profile/jing.hwa.tu/viz/IndeedDataAnalystScrapedJobs/Dashboard1?publish=yes).)

This project scrapes job postings for **Data Analyst** positions in Australia from Indeed. It extracts key information from the search pages (such as job titles, locations, and URLs) and then uses the individual job URLs to scrape detailed job descriptions. The data is then cleaned and merged into a final CSV file containing the following columns:

- **Job Title**
- **URL**
- **Company**
- **Location**
- **Job Description**
- **Suburb**
- **State**
- **Postcode**

This structured CSV file is designed for further analysis and visualization in tools like Tableau, as well as for use in job application processes. (For more details on the job application process, please refer to my other repository: [job_application_project](https://github.com/fafadu/job_application_project).)

Additionally, this project includes a basic Tableau visualization showcasing 208 job postings.

## Repository Structure

- **README.md**: This documentation file.
- **indeed_jobs_merged.csv**: The final merged CSV file containing the cleaned job data.
- **merging_data_cleaning.ipynb**: Jupyter Notebook for merging and cleaning the scraped data.
- **scape_title_url.ipynb**: Jupyter Notebook for scraping job titles and URLs from Indeed.
- **scrape_job_description.ipynb**: Jupyter Notebook for scraping detailed job descriptions using the job URLs.

## How It Works

1. **Scraping Job Listings**:
   - The `scape_title_url.ipynb` notebook uses Selenium (with undetected-chromedriver) to navigate Indeed's search pages.
   - It extracts the job titles, locations, and URLs from multiple pages of results.

2. **Scraping Job Descriptions**:
   - The `scrape_job_description.ipynb` notebook visits each job URL to scrape the detailed job descriptions.

3. **Data Cleaning and Merging**:
   - The `merging_data_cleaning.ipynb` notebook cleans and merges the data from the two scraping processes.
   - The final output is stored in `indeed_jobs_merged.csv` with the columns: Job Title, URL, Company, Location, Job Description, Suburb, State, and Postcode.

3. **Visualization:**:
Use the resulting indeed_jobs_merged.csv as ata source for Tableau.
Refer to the included Tableau visualization for an example overview of 208 job postings.

## Prerequisites

- **Python 3.x**
- Required Python packages:
  - `selenium`
  - `undetected-chromedriver`
  - `pandas`
  - Standard libraries such as `time` and `random`

*Note: The notebooks include installation instructions for the necessary packages if they are not already installed in your environment.*

## Setup and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/fafadu/Indeed-data-scraping-and-visualization.git
   cd Indeed-data-scraping-and-visualization
