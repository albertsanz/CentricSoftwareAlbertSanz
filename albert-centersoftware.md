# Central Software Challenge - Step 2
# Model deployment on production
*Written by Albert Sanz*
### Deployment plan to setup the solution model into production environment

### 1. Craft Your Inaugural Model Version
Generate a foundational solution that's ready to scale. Your initial version should involve developing a model that delivers decent predictions, trained on an available dataset.
### 2. Establish a Code Repository
Where code meets version control. Consider platforms like GitHub or GitLab to maintain a structured versioning process for your project.
### 3. Keep Datasets in Check
Maintain a historical record of your datasets. Tools like DVC (Data Version Control) can help you manage different dataset versions over time
### 4. Local modeling version.
Optimize your model with grid search, finding the perfect parameter combination to create the most accurate model. Implement MLflow, storing model characteristics, performance metrics, and dataset version information. Stash these files in a secure location, such as AWS S3.
### 5.Elevate to the Cloud 
Give your models a unique version code for seamless management and linking to their corresponding MLflow files. 
Store your models in S3 repositories, set up Lambda functions for automated transfers to EFS (Elastic File System), where production machines can access them.
### 6. Embrace MLOps Tools and Integration
For advanced model management, consider Amazon SageMaker for performance monitoring and scaling. 
Use AWS CloudWatch to keep a vigilant eye on machine performance during training and production use.
### 7. Define and Monitor KPIs
Identify key performance indicators (KPIs) that can signal when your model isn't performing as expected. 
Set up CloudWatch Alarms to receive alerts when these KPIs deviate from the desired thresholds.
### 8. Automated testing 
Implement automated testing procedures for both your model and datasets. 
Create unit tests for your code, integration tests for your model, and performance tests at every stage of modeling, including training, validation, and testing.
### 9. Plan for Rollback
Every step of your deployment process should be thoroughly documented and version-controlled. This way, you can always trace back to see how you've evolved and ensure a transparent, replicable process.
### 10. Streamlined Documentation
Record the entire deployment process and maintain version control for a traceable history 

