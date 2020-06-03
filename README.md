# "1033" Program Transfers Post Ferguson

This repository analyzes the transfers made by the Defense Logistics Agency to local law enforcement since the protests in Ferguson, MO in August 2014 in support of the June TKTK, 2020 BuzzFeed News story TKTKTKTK. 

The DLA is a sub-agency of the Department of Defense that provides equipment to local law enforcement agencies through its Law Enforcement Support Office. The program is commonly referred to as the "1033" program due to the statute that created it in 1997.

## Data

The data used in this analysis comes from the DLA's [LESO Public Information](https://www.dla.mil/DispositionServices/Offers/Reutilization/LawEnforcement/PublicInformation/) page. The `[data/all.xlsx]("/data/all.xlsx")` file contains all property transferred to participating agencies that was held by them as of March 31, 2020. It is updated quarterly.

## Notebooks

### Data Conversion

The `[convert-1033-data-excel.ipynb]("/notebooks/convert-10333-data-excel.ipynb")` notebook takes the Excel file the DLA produces, reads each of the 52 sheets, and combines them into a single CSV with all the available data. The resulting CSV file is output to `[outputs/dla-1033-transfers.csv]("/outputs/dla-1033-transfers.csv")`.

### Analysis

The `[1033-transfers-post-ferguson.ipynb]` takes the CSV data and analyzes all transfers where the `Ship Date` is after August 25, 2014, which was the end of the protests in Ferguson, MO. It walks through a few different pieces of analysis, including:

- Loading the data
- Filtering for transfers post August 25, 2014
- Totaling the transfers
- Going through analysis of items in support of the story

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). Files in the `output/` directory are available under the [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/).

## Contact

If you have any questions about this repository you can reach out to John Templon at [john.templon@buzzfeed.com](john.templon@buzzfeed.com).

Looking for more from BuzzFeed News? [Click here for a list of our open-sourced projects, data, and code](https://github.com/BuzzFeedNews/everything).