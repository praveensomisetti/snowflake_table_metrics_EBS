# snowflake_table_metrics_EBS
Metrics created from Snowflake DB tables and deployed in AWS using EBS

1. Create a procfile with this command-  web: streamlit run app.py --server.port 8000
2. Zip the Required folders along with .env file.. including .env file is optional.. either we can zip from here or else we can add later
3. In AWS open EBS: Amazon Elastic Beanstalk


Deploying Streamlit App on AWS Elastic Beanstalk
Steps:
Compress and Zip the Streamlit Application
Prepare your application files:
Example: app.py requirements.txt with all the required dependencies
Create a new file in the project with the filename Procfile with content
web: streamlit run app.py --server.port 8000
• Add the above command to the Procfile.
• Select all necessary project files and compress them into a zip file: In our case: app.py, requirements.txt, and Procfile
Create the Elastic Beanstalk Environment in the AWS Console
• Search for Elastic Beanstalk in the AWS Console.
• Select "Create Environment".
Environment Tier
• Select "Web server environment".
Application Information
• Enter your preferred Application name, e.g., Streamlit-App.
Environment Information
• Enter your preferred Environment name, e.g., ABCD Dashboard env.
• Enter your preferred Domain name, e.g., ABCD Dashboard.
Platform
• Choose "Managed Platform".
• Select the platform Python.
• Choose the preferred platform branch.
• Select the suitable platform version.
Application Code
• Choose "Upload your code".
• Enter the version, e.g., V1.
• Select "Local file".
• Upload the compressed zip file of your project application. Note: All files should be in the root directory (select all files inside the project, zip them, and upload).
Step II: Configure Service Access
• Create or select the required service roles.
Step III: Set Up Networking, Database, and Tags
• This step is optional and should be set up as needed.
Step IV: Configure Instance Traffic and Scaling
• This step is optional and should be set up as needed.
Review and create the environment.
Re-Deployment
• If there are any code changes, zip the files again as mentioned above.
• Open the AWS Console.
• Search for Elastic Beanstalk.
• Select the previously created Environment Name.
• In the top right, you will see the option "Upload and Deploy"; select this option.
• Change the version and upload the new zip file.
