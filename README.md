# Splunk-Query
This repo is about the basic use of Splunk by the Google Cybersecurity Certificate course. It records how I use the SPL to search the log data needed for the course.

## Upload Data for analysis
- Select the "Add Form" from "Setting"
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/7f0187d6-887f-4304-8d12-0724b3613fae)

![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/cd3aa2f8-bef6-4495-8556-f1c13cf003fd)

![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/49b5b57c-93c4-47d1-bf97-baaed5ec6c7a)


## Query for data
- Choose the "Search and Reporting"
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/093ee8d3-6fe5-4464-b282-4243295700ba)

- Input the `index="main" ` SPL in the field to search
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/0b07a311-df82-49b1-98e6-58d6f5b3720d)

![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/7e1ea379-e757-44d4-9d05-bb3ebfe5a097)


### Search only from mailsv host
- `index="main" host="mailsv" fail* root ` to find the data from mailsv and contain fail  and root text in the log.
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/a8e5a03d-1203-4b2c-8a69-7bf7665c0239)

- This search expands on the search from the previous task and searches for the keyword fail*. The wildcard tells Splunk to expand the search term to find other terms that contain the word fail such as failure, failed, etc. Lastly, the keyword root searches for any event that contains the term root.
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/006fed3f-5c6a-4e1a-a0c3-c0701828e636)


### Search for web cookie through "sourcetype"
- `index="main" sourcetype="access_combined_wcookie"` to search the source from access_combined_wcookie
![image](https://github.com/leonlamsc/Splunk-Query/assets/140391766/43833ed0-1bdd-4a91-b8d3-15d823685055)
