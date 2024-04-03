# scraping_naukridata
## Scraping Job role and Job loction from naukri website
### Installation
1.selenium
2.beautifulsoup
### programme working
1.we should provide url where we want scrap the data.
2.selenium create a virtual or new chrome website with the url which makes easy to scrap.
3.driver key is used to retrive or get the data from the website
4.beautifulsoup is used find the required text from the html code.
5.save the data in different variable(job role,job location and job name..)
### code
1.from selenium import webdriver
2.from bs4 import BeautifulSoup

3.driver = webdriver.Chrome()
4.driver.get("https://www.naukri.com/fresher-jobs?src=gnbjobs_homepage_srch")
5.soup=BeautifulSoup(driver.page_source,'html.parser')

6.name = "row1"
7.location= "ni-job-tuple-icon ni-job-tuple-icon-srp-location loc"

8.company_names=soup.find_all(class_=name)
9.company_location=soup.find_all(class_=location)

10.job_title=[]
11.for i in company_names:
12    job_title.append(i.text)

13.job_location=[]
14.for i in company_location:
15.    job_location.append(i.text)

16.job_title
17.job_location
