Imported necessary libraries: selenium, BeautifulSoup, pandas, matplotlib.
Used Chrome WebDriver 
Scraped job details including:
	Job Title
	Company Name
	Salary
	Skills
	Location
(Location scraping was tricky due to nested HTML — solved with Google search & trial-and-error parsing)
	Scraped first 5 pages of job listings.
	Stored results into a Pandas DataFrame for easy handling.
Results:
	215 jobs found across first 5 pages.
	Top 5 job locations identified.
	Top 10 in-demand skills extracted.
	Visualization:
	Bar chart for top 5 job locations.
	Pie chart for job distribution across locations.

Visuals
Top 5 Job Locations (Bar Chart)
 
Distribution of Jobs by Location (Pie Chart)
 

Challenges Faced
Dynamic content loading → used time.sleep() and scrollTo to ensure data was fully loaded.
Location extraction → required handling nested tags (<p> with <span> and <a> elements).
Skills parsing → initially concatenated strings incorrectly, later fixed by extracting each <a> tag.
Maximize window issue → replaced with set_window_size() since headless mode doesn’t support maximize_window().

