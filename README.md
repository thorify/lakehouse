# Lakehouse

This project provides a comprehensive Lakehouse implementation which uses technologies like Apache Spark, Jupyter Notebook, MLflow, and Apache Zeppelin. The aim is to bridge the gap for data professionals who have experience with Python and libraries like pandas, but find transitioning to Spark or paid cloud solutions like Databricks challenging.

This project serves as an introductory platform, designed to make the transition smoother and more intuitive. It is being developed alongside a series of [Medium articles](https://medium.com/@piotrblakala) which provide detailed explanations and guides to understanding and utilizing this project.

## How to Run

1. Clone the repository: `git clone https://github.com/thorify/lakehouse.git`
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

Jupyter Notebook serves as the interactive development environment for data processing and analysis. This Docker image is custom-built by the author, based on the official Jupyter Docker image. The Dockerfile and further documentation can be found in the [author's Docker Hub repository](https://hub.docker.com/repositories/zirael44).

### MLFlow

MLFlow is an open source platform for managing the end-to-end machine learning lifecycle. It is not used extensively in the initial stages of this project, but it will feature more prominently in the future as the project develops. The Docker image used in this project is custom-built by the author, with further documentation and Dockerfile available in the [author's Docker Hub repository](https://hub.docker.com/repositories/zirael44).

### Apache Zeppelin

Apache Zeppelin is a web-based notebook that enables data-driven, interactive data analytics and collaborative documents with SQL, Scala, and more. The custom-built Docker image used in this project is based on the official Apache Zeppelin Docker image. Additional documentation and Dockerfile can be found in the [author's Docker Hub repository](https://hub.docker.com/repositories/zirael44).

## Notebooks

This project contains two example notebooks: one in Zeppelin and one in Jupyter Notebook. These notebooks demonstrate the basic functionalities of the environment and Spark, using weather data from Visual Crossing as an example dataset.

## Contribution

This project is still under development and contributors are always welcome. Feel free to submit a pull request or create an issue.

## License

This project is licensed under the terms of the MIT license. See the [LICENSE](https://github.com/thorify/Lakehouse/blob/main/LICENSE) file for license rights and limitations.
