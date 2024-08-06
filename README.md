# Super Fun DMN tutorial
So you want to learn about DMN? what about DRDs? FEEL? BKM? - well all those acronyms and more will be explained over the course an ever expanding DMN example. Currently in 4 parts. 
1. Building a DMN table
1. Executing DMN with a BPMN model
1. Creating Literal Expressions and BKMs
1. Building Advanced DMN Tables

Each part will expand on the previous but you an kick off by downloading from this repo the models required for the example you're interested in.

### How to Run the Examples
You’ll need a Camunda 8 Cluster (the easiest place to do that is[ Camunda SaaS](http://camunda.io/)). Then the fun can start!
In each folder their'll be the required, DMN, BPMN and Form files. Upload them into a folder in the Camunda Modeler and use the `Deploy` button so that you can run them. 

## Part 1: Building a DMN table 
In this example we're trying determine if a user is eligible for an upgrade to a mysterious account that they have. Based on some user criteria we'll return a true or false result

![DMN Table](./Part1-DMN-Table/DMNTable.png)
 
### Part 2: Executing DMN with a BPMN model
This example integrates your DMN table with a BPMN model. We do this so that we can create forms for users to fill out, the data of which will be given to the DMN table and then the result can be viewed in another form. 

![BPMN Model](./Part2-DMN-BPMN-Integration/BPMNModel.png)

### Part 3: Creating Literal Expressions and BKMs
Here we introduce the concept of a Decision Requirements Diagrams (DRDs) which help give better context to a DMN table's execution. 
DRDs include a Literal Expression which is used when you need to make some kind of calculation with FEEL (Friendly Enough Expression Language) and Business Knowledge Models (BKM) which can used to write reusable functions.

In this case we have a BKM in which you can give someone's data of birth and it will return `true` or `false`
The Literal Expression uses this function un order to create a variable that's used in our original table. 

![DRD Model](./Part3-DRD-Literal-Expressions/DRD.png)

### Part 4: Building Advanced DMN Tables
Now we're going to add a second DMN table to our DRD - but this one is a little more complicated. Its going to calculate the `Engagement Score` for a user given a bunch of input variables. 

![EngageDRD](./Part4-Complex-DMN-Table/CalcEngagementDRD.png)

### THE END
(hope you had fun)