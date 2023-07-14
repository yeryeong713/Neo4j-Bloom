# Neo4j-Bloom   
Neo4j Bloom Movie Visualization with Neo4j Aura DB

## Project Description
This project focuses on utilizing Neo4j Bloom and Neo4j Aura DB to create visually appealing and interactive visualizations of movie networks. The dataset encompasses information about movies and the individuals associated with them, including actors, directors, producers, and writers. By employing a series of query statements, the project aims to extract relevant information and generate diverse visual representations. With this project, users can explore the intricacies of movie networks and gain insights into the relationships between movies and people.

### Visualize with Neo4j Bloom
![movie](https://github.com/yeryeong713/Neo4j-Bloom/assets/88486391/dfd610a5-f4e4-470d-92d4-59fe39d846cf)

### Query examples
-  List all Tom Hanks movies :
     
    MATCH (tom:Person {name: "Tom Hanks"})-[:ACTED_IN]->(tomHanksMovies) RETURN tom,tomHanksMovies
   ![query](https://github.com/yeryeong713/Neo4j-Bloom/assets/88486391/4fcb6f67-5f22-4ceb-a16f-00892808344c)


- Who directed "Cloud Atlas"? :
     
   MATCH (cloudAtlas {title: "Cloud Atlas"})<-[:DIRECTED]-(directors) RETURN directors.name
![query1](https://github.com/yeryeong713/Neo4j-Bloom/assets/88486391/9f542458-3046-4e0b-b095-1def1c12db75)

- How people are related to "Cloud Atlas" :
        
  MATCH (people:Person)-[relatedTo]-(:Movie {title: "Cloud Atlas"}) RETURN people.name, Type(relatedTo), relatedTo
![query2](https://github.com/yeryeong713/Neo4j-Bloom/assets/88486391/dea69c1d-0061-4e8d-9e31-78fc8d78f72e)
