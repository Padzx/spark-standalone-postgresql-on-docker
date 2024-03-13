# [1.0.0] - 2024-02-29 

## Added 

- Pushed Image Base OpenJDK-11 to Docker Hub

## Details 

- Created Image Dockerfile OpenJDK and configuring the enviroment (**folder base**).

- Update the Dockerfile to include necessary dependencies for spark application.

- Configured workflow to log in to Docker Hub using secrets stored in Github.

- Built and tagged the OpenJDK image with the latest version.

- Pushed the tagged image to the Docker Hub Repository.


# [1.0.0] - 2024-02-29 

## Added

- Pushed Image Spark Base to Docker Hub

## Details

- Created Image Dockerfile Spark-Base based in OpenJDK Image (**folder spark-base**).

- Updated the Dockerfile to include necessary dependencies (included spark postgresql.jar file) for spark application and clusters master and worker

- Configured workflow to log in to Docker Hub using secrets stored in Github.

- Built and tagged the Spark image with the latest version.

- Pushed the tagged image to the Docker Hub Repository.

# [1.0.0] - 2024-03-01

## Added 

- Building Spark Clusters Master and Worker

## Details 

- Created Image Dockerfile Spark Master Cluster based in spark-base (**folder spark-master**).

- Created Image Dockerfile Spark Worker Cluster based in spark-base (**folder spark-worker**).

- Updated the Dockerfile Spark Master and Worker Clusters to included necessary dependencies for spark clusters application.

- Configured workflow to log in to Docker Hub using secrets stored in Github.

- Built and tagged the Spark image clusters with the latest version.

- Pushed the tagged image to the Docker Hub Repository.


# [1.0.0] - 2024-03-01

## Added 

- Building Image Jupyter Lab 

## Details

- Created Image Dockerfile Jupyter Lab Image based in OpenJDK-11 (**folder jupyter-lab**).

- Updated the Dockerfile Jupyter Lab necessary (like pyspark, pandas, findspark, etc) dependencies for spark and postgresql connections application.

- Configured workflow to log in to Docker Hub using secrets stored in Github.

- Built and tagged the Jupyter Lab image clusters with the latest version.

- Pushed the tagged image to the Docker Hub Repository.

# [1.0.0] - 2024-03-03

## Added 

- Building Image PostgreSQL

## Details

- Created Image Dockerfile PostgreSQL image (**folder postgresql**).

- Updated the Dockerfile PostgreSQL necessary dependencies for spark and postgresql connections application.

- Configured workflow to log in to Docker Hub using secrets stored in Github.

- Built and tagged the PostgreSQL image clusters with the latest version.

- Pushed the tagged image to the Docker Hub Repository.

# [1.1.0] - 2024-03-13

## Added

- Building Image JupyterLab

## Details 

- Updated Image JupyterLab Image

- Insert Tutorial About, How Testing Connection of Clusters Spark and connection wit PostgreSQL Database  