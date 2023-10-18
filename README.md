# DealValidation Script

## Overview

This script, named **DealValidation**, is designed to interact with the Pipedrive API to manage and validate deals. The main functionalities include accessing Pipedrive through its API, retrieving information about organizations and deals, and continuously updating deal data.

## Table of Contents
- [Overview](#overview)
- [Data Retrieval](#data-retrieval)
- [Website Validation](#website-validation)
- [Database Setup](#database-setup)
- [Pipedrive API Integration](#pipedrive-api-integration)
- [Additional Features](#additional-features)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Execution](#execution)

## Data Retrieval

1. **Data Retrieval:**
   - The script fetches information from Pipedrive, specifically organizations and deals.
   - It constructs the **DealValidation** table, linking organizations with deals and associating each company's website with its corresponding deal.

## Website Validation

2. **Website Validation:**
   - A function called `get_status` checks the validity of each organization's website.
   - Invalid websites are flagged, and their corresponding deals are marked as "lost," removing them from the sales funnel.

## Database Setup

3. **Database Setup:**
   - The script creates and maintains a SQLite database (`pipedrive.db`) to store organization and deal data.

## Pipedrive API Integration

4. **Pipedrive API Integration:**
   - It utilizes the Pipedrive API to access and update information.
   - Pipedrive credentials (API token) are required for authentication.

## Additional Features

5. **Additional Features:**
   - The script uses multithreading for efficient processing.
   - It includes error handling for various scenarios, such as timeouts and exceptions.

## Usage

6. **Usage:**
   - To execute the script, fill in your Pipedrive API token in the `your_token` variable.
   - Ensure the necessary Python packages (`requests`, `json`, `pandas`, `concurrent.futures`, `sqlite3`) are installed.

## Code Structure

7. **Code Structure:**
   - The script is organized into sections for better readability and maintenance.
   - Sections include importing packages, defining API details, creating functions, setting up database tables, and more.

## Execution

8. **Execution:**
   - Save the script as a Python file (e.g., `deal_validation_script.py`).
   - Open a terminal and navigate to the script's directory.
   - Run the script using `python deal_validation_script.py`.

Note:

