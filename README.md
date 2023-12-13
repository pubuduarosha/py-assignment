# Pubudu Wanigasekara - Pre Interview Assessment

## Test 1:

### Requirements
- Python 3.x

### Steps to Run Test 1
1. **Service Monitoring and JSON Creation**
    - Run the provided Python script `Test1_and_Test2.ipynb` to monitor services (`httpd`, `rabbitMQ`, `postgreSQL`) and create JSON objects for each service status.

2. **REST Service Setup**
    - Run the Flask-based Python script `Test1_and_Test2.ipynb` to create endpoints for:
        - `/add` to insert payload into Elasticsearch
        - `/healthcheck` to retrieve overall application status
        - `/healthcheck/{serviceName}` to retrieve specific application status

3. **Usage Examples**
    - Use sample calls to interact with the REST service:
        - `https://myservice.example.com/add`
        - `https://myservice.example.com/healthcheck`
        - `https://myservice.example.com/healthcheck/httpd`

## Test 2

### Steps to Run Test 2
1. **Ansible Inventory Setup**
    - Create an inventory file (`hosts.ini`) with details of target hosts for services (`httpd`, `rabbitMQ`, `postgreSQL`).

2. **Execute Ansible Playbook**
    - Run the provided Ansible playbook `playbook.yml` using the command:
        ```
        ansible-playbook playbook.yml -i hosts.ini -e action=<action_here>
        ```
        Replace `<action_here>` with:
        - `verify_install`: Verify and install services if not present
        - `check-disk`: Check disk usage on servers and send alerts if > 80%
        - `check-status`: Check the status of 'rbcapp1' and services

3. **Modify Variables if Needed**
    - Update variables in the playbook as per your environment (e.g., email recipients, service endpoints).


## Test 3

## Files
- `assignment data.csv`
- `Test3.ipynb`

## Usage
1. Ensure Python is installed on your system.
2. Place the `assignment data.csv` file in the directory: `data`.
3. Run the `Test3.ipynb` script using a Jupyter interpreter.

## Functionality
- The Python script reads the `assignment.csv` file.
- It calculates the price per square foot for each property.
- Filters out properties that were sold for less than the average price per square foot.
- Generates a new CSV file named `filtered_properties.csv` containing the filtered data.

