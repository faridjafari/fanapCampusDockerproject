Docker Elasticsearch Kibana Project Documentation
Overview
This documentation outlines the process of setting up Elasticsearch and Kibana using Docker Compose. The project aims to provide a streamlined method for deploying and managing Elasticsearch and Kibana instances for various use cases.

Project Objectives
Deploy Elasticsearch and Kibana containers using Docker Compose.
Configure Elasticsearch and Kibana to use specific versions (8.0.1).
Ensure Elasticsearch and Kibana are accessible via specified ports.
Implement health checks to monitor the status of the Elasticsearch container.
Utilize volume for data management and network configuration for container communication.
Resolve Docker Hub access restrictions for users in restricted regions.
Steps Taken
1. Docker Compose Configuration
Created a docker-compose.yml file defining Elasticsearch and Kibana services.
Specified Elasticsearch and Kibana versions as 8.0.1.
Configured ports for Elasticsearch (9200) and Kibana (5601).
Implemented a health check for Elasticsearch to monitor container status every 30 seconds.
2. Volume and Network Configuration
Utilized volume for data management, ensuring persistence of Elasticsearch data.
Placed Elasticsearch and Kibana services in the same network (docker-elastic-kibana_elastic).
Configured the network's driver as bridge with a custom subnet range (172.25.0.0/24).
3. Docker Daemon Configuration
Addressed Docker Hub access restrictions by adding insecure registries and registry mirrors to Docker daemon configuration.
4. Project Completion and Documentation
Tested and verified project functionality, ensuring Elasticsearch and Kibana services are accessible.
Added project to a GitHub repository for version control and collaboration.
Documented project setup, encountered problems, and solutions for future reference.
Encountered Problems and Solutions
Problem: Docker Hub Access Restriction
Users in restricted regions faced Docker Hub access restrictions, hindering image retrieval.
Solution: Added insecure registries and registry mirrors to Docker daemon configuration to bypass access restrictions.
Problem: Unclosed Action Error in Health Check Command
Error (unclosed action) occurred while inspecting Elasticsearch container health status.
Solution: Simplified health check command to directly inspect health status without template syntax, resolving the error.
