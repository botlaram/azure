# azure web app service

1. do az login

2. create resource group

3. create dir

4. cd dir > git clone this repo

5. run > az webapp up -g $resourceGroup -n $appName --runtime "PYTHON:3.9" --location CentralUS
this will create web app service and zip src code, it will recognize that the src is python structure as py and requirements.txt will be present.

6. it will show the following logs and url hosted to access flask app

```logs
ramakrishnabotla04 [ ~/demo/azure ]$ az webapp up -g $resourceGroup -n $appName --runtime "PYTHON:3.9" --location CentralUS
Webapp 'az204app18227' already exists. The command will deploy contents to the existing app.
Creating AppServicePlan 'ramakrishnabotla04_asp_5823' or Updating if already exists
Readonly attribute name will be ignored in class <class 'azure.mgmt.web.v2023_01_01.models._models_py3.AppServicePlan'>
Creating zip with contents of dir /home/ramakrishnabotla04/demo/azure ...
Getting scm site credentials for zip deployment
Starting zip deployment. This operation can take a while to complete ...
Deployment endpoint responded with status code 202
Polling the status of async deployment. Start Time: 2024-08-25 13:44:55.291459+00:00 UTC
Status: Building the app... Time: 3(s)
Status: Building the app... Time: 19(s)
Status: Build successful. Time: 36(s)
Status: Starting the site... Time: 52(s)
Status: Site started successfully. Time: 69(s)
You can launch the app at http://az204app18227.azurewebsites.net
Setting 'az webapp up' default arguments for current directory. Manage defaults with 'az configure --scope local'
--resource-group/-g default: learn-e2a9e9ac-ede2-4607-8219-42db48e581fa
--sku default: F1
--plan/-p default: ramakrishnabotla04_asp_5823
--location/-l default: centralus
--name/-n default: az204app18227
{
  "URL": "http://az204app18227.azurewebsites.net",
  "appserviceplan": "ramakrishnabotla04_asp_5823",
  "location": "centralus",
  "name": "az204app18227",
  "os": "Linux",
  "resourcegroup": "learn-e2a9e9ac-ede2-4607-8219-42db48e581fa",
  "runtime_version": "PYTHON|3.9",
  "runtime_version_detected": "-",
  "sku": "PAID",
  "src_path": "//home//ramakrishnabotla04//demo//azure"
}
```
