# Master cloud apps TFM - Infrastructure

## Table of contents
- [Master cloud apps TFM - Infrastructure](#master-cloud-apps-tfm---infrastructure)
    - [Table of contents](#table-of-contents)
    - [Description](#description)
    - [Requirements](#requirements)
    - [Technologies](#technologies)
    - [Project structure](#project-structure)
    - [Configuration](#configuration)
    - [Usage](#usage)
    - [Developers](#developers)

## Description
This is the Master cloud apps TFM infrastructure repository.
It contains the necessary infrastructure resources to deploy TFM project:
* MySQL instance for [Users API](https://github.com/mca-tfm/users).
* Dynamodb tables for [Products API](https://github.com/mca-tfm/products).

## Requirements
No necessary requirements.

## Technologies
* [AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html): AWS CloudFormation is a service that helps you model and set up your AWS resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS.

## Project structure
Project is composed by the next modules:
* **cloud**: contains docker files
  * **aws**:
    * **cloudFormation**: 
      * **tfm-stack.yml**: cloud formation stack template to create necessary AWS resources for the TFM project.
* **docs**: folder with TFM project documentation.
  * **demo**: demo resources.
  * **LICENSE**: Creative Commons Attribution Share-Alike license.
  * **memory.docx**: editable memory document.
  * **memory.pdf**: editable memory document.
  * **slides.key**: slides in key format.
  * **memory.pdf**: slides in pptx format.
* **LICENSE**: Apache 2 license file.
* **README.md**: this file.

## Configuration
When load the stack template you'll have to introduce next parameters:
* **DBPassword**: Users API MySQL instance password.

## Usage
* This project is used only to create necessary resource for production environment (preproduction environment uses docker containers deployed on pre cluster k8s).
* Create an AWS CloudFormation stack following steps described in [AWS doc](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html#GettingStarted.Walkthrough.createstack)
using the template [tfm-stack.yml](cloud/aws/cloudFormation/tfm-stack.yml).
* Check resources creation status as described [here](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html#GettingStarted.Walkthrough.monitor).
* When stack creation finish, you can read necessary info as MySQL url in stack Outputs.

## Developers
This project was developed by:

👤 [Álvaro Martín](https://github.com/amartinm82) - :incoming_envelope: [amartinm82@gmail.com](amartinm82@gmail.com)
