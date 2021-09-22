# Sample AWS CloudFormation Templates

Use these sample AWS **CloudFormation** templates to learn and deploy your specific use cases. These all templates are designed in such a way that we can use these teamplates from understand the bascis of cloudformation to leveraging these templates into productions environments. Please note,  before launching a template, always review the resources that it will create and the permissions it requires.


# Some Best Practises To Follow during creation of CFN templates

Before you run execute a template in a production environments, we suggest that you follow these guidelines .

-   Test your template. Can you successfully create a stack with it? When you create a stack, AWS CloudFormation uses the  `ValidateTemplate`  API to check your template. When you delete a stack, is the stack (and all of its resources) successfully deleted? Make sure users aren't left with stray resources or stacks that have deletion errors.
-   In the Description section, add a brief description of your template. The description should indicate what the template does and why it's useful. For example:  `Description: "Create a LAMP stack using a single EC2 instance and a local MySQL database for storage. This template demonstrates using the AWS CloudFormation bootstrap scripts to install the packages and files necessary to deploy the Apache web server, PHP, and MySQL when the instance is launched."`
-   Format your template to make it human readable:
    -   Err on the side of human readability. If it makes your template easier to read, do it.
    -   Use a linter. There isn't one specific tool that we use. Whatever you use, make sure it also checks for syntax errors.
    -   Consider using two-space indents to reduce line wrapping.
-   Review IAM resources. If you include IAM resources, follow the standard security advice of granting least privilege (granting only the permissions required to do a task).
-   Remove secrets/credentials from your template. You might hardcode credentials or secrets in your template when you're testing. Don't forget to remove them before submitting your template. You can use this tool to help you scrub secrets:  [https://github.com/awslabs/git-secrets](https://github.com/awslabs/git-secrets).
-   Add your template to the correct folder so that others can discover it. If your template demonstrates a particular service, add it to the Services folder. If it uses multiple services to address a particular use case, add it to the Solutions folder.

# Additional Resources
To view all the supported AWS resources and their properties, see the  [Template Reference](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html).



