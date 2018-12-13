# Jupyter Oracle Autonomous Data Warehouse Dockerfile

Dockerfile that runs a Jupyter Notebook that can connect to your Oracle Autonomous Data Warehouse.

## Built With

* [Python 3](https://www.python.org/)
* [Jupyter](http://jupyter.org/)
* [Docker](https://www.docker.com/)
* [Oracle Autonomous Data Warehouse](https://cloud.oracle.com/en_US/datawarehouse)

## Prerequisites

You will need the following things properly installed on your computer:

* [Git](http://git-scm.com/)
* [Docker](https://www.docker.com/)
* [Oracle Autonomous Data Warehouse Instance](https://cloud.oracle.com/en_US/datawarehouse)

## Installation

* run `git clone https://github.com/caseyr003/jupyter-adw.git`

## Setup

Getting the Autonomous Data Warehouse Wallet files
* Navigate to your ADW instance on the Oracle Cloud Infrastructure Console
* Click 'DB Connection'
* Download the Client Credentials (Wallet)
* Unzip the files and place them in the `wallet` folder in this project

Adding python packages
* Update `requirements.txt` with desired pip packages

## Running

To run the project locally follow the following steps:

* change into the project directory
* `docker build -t jupyter/oracleadw .`
* `docker run -p 8888:8888 --name jupyter-adw jupyter/oracleadw`
* copy the link specified with the token after running (ex. http://127.0.0.1:8888/?token=94f4633307f858f5a59509dfb6c9a0c64efceb097e1ddcd0)
* update `oracle_adw` notebook with your ADW credentials
