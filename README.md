# github_bangalore_user_data
Scrapping GitHub user data in Bangalore data 

## Explanation of Data Scraping Script
This script uses the GitHub API to scrape data about users and their repositories in Bangalore.

1. Constants:

-Defines API URL, access token (needs to be kept private), headers with authorization token.

-Sets location to "bangalore" and minimum follower threshold (100).

-Sets repository page size to retrieve data in chunks (100).

2. Functions:

-get_users_in_bangalore fetches users with location "bangalore" and follower count above threshold, iterating through pages until no more results.

-get_user_details retrieves detailed information about a specific user using their username.

-get_user_repositories retrieves a user's public repositories, paginating until 500 repositories are collected or no more exist.

-clean_company_name removes special characters and converts company names to uppercase for consistency.

-save_to_csv saves user and repository data to separate CSV files.

3. Main Function:

-Initializes empty lists for user and repository data.

-Calls get_users_in_bangalore to get a list of users.

-Loops through each user:

-Fetches detailed user information using get_user_details.

-Extracts relevant data and creates a dictionary representing the user.

-Calls get_user_repositories to retrieve user's repositories.

-Loops through each repository:

-Creates a dictionary with relevant repository details.
Appends user and repository data dictionaries to respective lists.
Calls save_to_csv to write the collected data to CSV files.
