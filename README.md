# Neo4j-Bloom   
Neo4j Bloom Movie Visualization with Neo4j Aura DB

## Project Description
This project focuses on utilizing Neo4j Bloom and Neo4j Aura DB to create visually appealing and interactive visualizations of movie networks. The dataset encompasses information about movies and the individuals associated with them, including actors, directors, producers, and writers. By employing a series of query statements, the project aims to extract relevant information and generate diverse visual representations. With this project, users can explore the intricacies of movie networks and gain insights into the relationships between movies and people.

### Visualize with Neo4j Bloom
![movie](https://github.com/yeryeong713/Neo4j-Bloom/assets/88486391/dfd610a5-f4e4-470d-92d4-59fe39d846cf)

### Query examples
-  List all Tom Hanks movies :
     
    MATCH (tom:Person {name: "Tom Hanks"})-[:ACTED_IN]->(tomHanksMovies) RETURN tom,tomHanksMovies

- Who directed "Cloud Atlas"? :
     
   MATCH (cloudAtlas {title: "Cloud Atlas"})<-[:DIRECTED]-(directors) RETURN directors.name

- How people are related to "Cloud Atlas" :
        
  MATCH (people:Person)-[relatedTo]-(:Movie {title: "Cloud Atlas"}) RETURN people.name, Type(relatedTo), relatedTo
