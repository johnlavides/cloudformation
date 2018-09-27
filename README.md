# cloudformation
This repo is for the Cloudformation Template with VPC, AutoScaling Group, ELB to serve traffics from the instances using port 8080.

Note: Before creating stack. An existing key-pair is required.

How to create the stack on the Cloudformation using this template

- Login to your aws console
- On the services drop-down select the "Cloudformation"
- Select the "Create new stack"
- Supply the Stack Name, Environment Name, CIDR and other details needed. (Note: T2, and T1 Instance type will not work in other Region, Use the M3 or M2 instance Type)
- Select next when you are done supplying the details needed and you will go to the next page.
- Expand the advance and look for the "Termination Protection" options and enable it. (It is a best practice to enable it to avoid accidental deletion of stack)
- Select next and check the Acknowledge the creation of cloudformation template and select "Create"
- After you select the "Create" you will be redirected to a stack page where you can see the name of the stack you created and you will also see a list of stack that was created(If there are any)
- Wait for the services to be created/completed. You can track the status on the events tab of your stack. You can also use this to check if there are error encounter during the creation of stack.

View the details of the stack you created

- Select the name of the stack you created
- Select the "Output" tab
- You can now see the list of the details created of your stack including the url to test the elb where you can use to run in your browser to test the traffics from the instances using port 8080
