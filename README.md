# cloudformation-project
  This is repo that hold files to create aws infrastructure and deploy satic web application.

## Setup
 1. Create a new user and assign adminprivileges(Should not be used for production).
 2. Give programatic access to users and generate a secrete key and password from aws console.
 3. In EC2 instances
    - Install aws CLI
        ```
        sudo apt  install awscli
        ```
        ```
         aws configure
          -  Aws access Key ID : <user-access-key>
          -  Aws Secret Acccess Key : <user-access-secret-key>
          -  Default region name : <region you want to pick e.g - us-west-2>
          -  output format : <leave it empty>
        ``` 
        ```
        aws s3 ls <If you see your list of resources(if available) , that means setup is done.>
        ```
## Run the project
 1. Run below commands to make create.sh executable 
    ```
    $ chmod +x create.sh
    ```
    ```
    $ ./create.sh infrastructure infrastructure.yml infrastructure-params.json
    ```
    ```
    $ ./create.sh networks networks.yml networks-params.json
    ```
    ```
     $ ./create.sh servers servers.yml servers-params.json
    ```
## Test
  1. Go to EC2 -> on left section -> Load Balancer 
  2. Copy and past the LB url on browser.
