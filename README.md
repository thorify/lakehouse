# Lakehouse

This project provides a comprehensive Lakehouse implementation which uses technologies like Apache Spark, Jupyter Notebook. The aim is to bridge the gap for data professionals who have experience with Python and libraries like pandas, but find transitioning to Spark or paid cloud solutions like Databricks challenging.

This project serves as an introductory platform, designed to make the transition smoother and more intuitive. It is being clone from a series of [Medium articles](https://medium.com/@piotrblakala) which provide detailed explanations and guides to understanding and utilizing this project.

## How to Run

1. Clone the repository: `git clone https://github.com/trongtran-agilityio/lakehouse.git`
2. If still not in navigate to the root directory of the project: `cd lakehouse`
3. Create the required local directory structure as a user to avoid potential write errors that may occur when root-level services first create directories on the host:

   ```bash
   mkdir -p ./app/data/output/delta
   mkdir -p ./app/data/output/spark-warehouse
   ```
4. Run the Docker Compose file: docker-compose up:

   ```bash
   docker-compose up
   ```
## Components

### Spark

This project uses Bitnami Docker Spark image as the base. Spark master and two workers are created, with configuration options set to allow for easier local development.

### Jupyter Notebook

Jupyter Notebook serves as the interactive development environment for data processing and analysis. This Docker image is custom-built by the author, based on the official Jupyter Docker image. The Dockerfile and further documentation can be found in the [author's Docker Hub repository](https://hub.docker.com/u/trongtran).

## How to Play Around

- [localhost:8889](http://localhost:8889): This will launch the JupyterLab environment. I intentionally changed the default port from 8888 to 8889, as many other services use 8888 by default, and I wanted to avoid conflicts.
- [localhost:8080](http://localhost:8080): Here, you can check the status of the Spark master service. You should also see the status and links for connected Spark workers.
- [localhost:38081](http://localhost:38081) and [localhost:38082](http://localhost:38082): These addresses will display the status of the spark-worker-1 and spark-worker-2 services.

## Contribution

This project is still under development and contributors are always welcome. Feel free to submit a pull request or create an issue.

## License

This project is licensed under the terms of the MIT license. See the [LICENSE](https://github.com/thorify/Lakehouse/blob/main/LICENSE) file for license rights and limitations.
