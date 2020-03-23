# Hyperldger Indy Testing environment
## Description
This is a simple testing environment for testing application developed using [Hyperledger Indy SDK](https://github.com/hyperledger/indy-sdk). It includes a docker image of [Indy's sample pool](https://github.com/hyperledger/indy-sdk/tree/master/ci) and instructions for using it. 

## Installation
### Prerequisites
In order to Install Indy's sample pool [docker](https://www.docker.com/get-started) is required. In order to be ample to run the example scripts you need fist to install [Indy SDK](https://github.com/hyperledger/indy-sdk#installing-the-sdk) and then the [python wrapper](https://github.com/hyperledger/indy-sdk#installing-the-sdk) 

Install the docker image of the sample indy pool by executing the following command inside the `test_pool` folder

* docker build -f indy-pool.dockerfile -t indy_pool .

## Running the sample
First run the Indy sample pool by executing:

* docker run --name test_pool -itd -p 9701-9708:9701-9708 indy_pool

Then execute

* python3 indy_sample.py