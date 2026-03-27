# About
We developed a four-phase TPSE-RCI framework to identify scientific research clusters: (1) Research Team Detection and Collaboration Network Construction, (2) Structural Representation Learning and Initial Cluster Identification, (3) Research Goal Extraction and Hierarchical Structuring, (4) Valid Research Cluster Identification.

# Citation
article：A novel scientific research cluster identification method integrating topological potential and semantic embedding


# Dataset Details
## 1. WOS.json
We constructed a structured dataset integrating bibliographic and author-level information from the Web of Science (WoS) database. Each record corresponds to a unique publication and includes identifiers, textual content, and author metadata. The key fields are summarized as follows:
| Field Name           | Type     | Description                                           |
|--------------------|---------|-------------------------------------------------------|
| ID                  | Integer | Unique identifier for each record in the dataset     |
| paper_id            | String  | Internal identifier for each publication            |
| WOS_ID              | String  | Unique Web of Science identifier for the publication|
| publication_year    | Integer | Year in which the article was published            |
| article_title       | String  | Title of the publication                             |
| abstract            | Text    | Abstract text describing the research content       |
| author_keywords     | String  | Author-provided keywords                              |
| DOI                 | String  | Digital Object Identifier for the publication       |
| author_id           | String  | Unique identifier assigned to each author           |
| author_full_name    | String  | Full name of the author as recorded in WoS          |
| ORCIDs              | String  | ORCID identifiers associated with the author        |
| Researcher_Ids      | String  | ResearcherID(s) identifiers associated with the author |
| addresses           | String  | Author affiliation addresses                         |


## 2. cluster_info.csv
This dataset records the identified research clusters and their associated structural information, including participating teams, authors, and research goals. Each row represents a single research cluster and its corresponding attributes. The dataset contains the following fields:
<table>
  <tr>
    <th style="white-space: nowrap;">Field Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>ID</td>
    <td>Integer</td>
    <td>Unique identifier of the record.</td>
  </tr>
  <tr>
    <td>cluster_id</td>
    <td>Text</td>
    <td>Unique identifier of the research cluster.</td>
  </tr>
  <tr>
    <td>valid</td>
    <td>Bool</td>
    <td>Indicates whether the cluster satisfies the defined validity criteria.</td>
  </tr>
  <tr>
    <td>team_list</td>
    <td>List</td>
    <td>List of teams involved in the cluster. Each element represents a unique team identifier.</td>
  </tr>
  <tr>
    <td>author_list</td>
    <td>List</td>
    <td>List of authors participating in the cluster. Authors may appear multiple times if they are associated with multiple teams.</td>
  </tr>
  <tr>
    <td>goal_list</td>
    <td>List</td>
    <td>List of research goals associated with the cluster. Each goal represents a specific research direction within the cluster.</td>
  </tr>
</table>

# Explanations and Issues
The release of this dataset is for research purposes only and should not be used for any inappropriate applications.
Certain data included herein are derived from Clarivate™ (Web of Science™). © Clarivate 2025. All rights reserved.
