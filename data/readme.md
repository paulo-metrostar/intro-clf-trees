# About the data
## This data was "synthesized"
- The data was synthesized to be classifiable (i.e. to have a signal a machine learning classifier can "tune in to.")
- The feature/columns were selected (and values were "massaged") to represent some intuitive features about a user's session on a website.

## Suppose we have data on a website's user-sessions
Including things like the time they accessed the site, the browser they are using, and which pages they visited and in which order. We also know what file they ultimately downloaded.

**In the real world you'll likely have many more features** for a session's record and they might require some cleaning and restructuring. But even if there are some noisy or redundant features a machine learning model can usually "tune in" to the ones that are "predictive" of the target you are trying to predict.
- **what the algorithm can do** much more efficiently for us is to measure and sort the features by their "correlation" to the target
- **what the algorithm can't do** is make judgement calls about which features are acceptably messy or redundant and which need to be refinend or cleaned.
    - For example, note that the boolean columns in our synthetic data set are not mutually exclusive, contrary to what you might expect (ex: the data may indicate the user used both firefox and chrome for the same session). This is merely an artifact of generating synthetic data, but for our "in fiction" purposes we can pretend they are the result of sloppy setup for the session tracking.

## data dictionary
- **start_hour** - a float between 0 and 24 representing the hours in a day
- **weekday** - an integer between 1 and 7 representing the days in a week
- **chrome_browser, firefox_browswer** - a boolean indicating whether the user accessed the site with a given browser
- **1st_page_search, 1st_page_faq** - a boolean indicating which page the user visited first during this session
- **2nd_page_search, 2nd_page_faq** - a boolean indicating which page the user visited second during this session
- **TARGET_DOWNLOAD** - an integer 0, 1, 2, indicating which of three available files a user downloaded at the end of their session