### Classification Proposal

**Purpose**

Animal shelters are places to find animal welcoming homes. With limited support, it is very important they utilize their resources effectively, so they can continue to do great work. By building a classification model to predict the adoption outcome, we can see which features contribute more to the positive outcome (will be explained below) and recommend them to the shelters, so they can distribute their resources accordingly.

**Data**

Animal Shelter Intake and Outcome from the Sonoma County, CA will be utilized. (https://data.sonomacounty.ca.gov/Government/Animal-Shelter-Intake-and-Outcome/924a-vesw).  The data currently has 21,673 rows and 24 columns.  However, I plan to work with 11 columns, and they are:

* Name of the animal
* Type of animal

* Breed
* Color
* Sex
* Size
* Date of Birth
* Which shelter the animal is currently located
* Days in shelter
* Reason for intake
* Animals' condition when leaving the shelter

With the current data, there are 8 outcome types, and they are:

* Adoption
* Return to owner
* Transfer to a different shelter
* Euthanized
* Appointment is made to interact with the animals
* Died
* Disposal
* Escaped/stolen

I would like to make the target of the project to two groups: 

* Positive outcome where animals actually find homes, and this includes adoption and return to owner
* Negative outcome where animals haven't find homes yet, and this includes the rest of the outcome types.

**Tools**

* Pandas for data cleaning and EDA
* Python packages for classification models for model building
* Matplotlib or Tableau for potential visualizaiton

**MVP Goal**

A MVP may include model(s) with the best performance score and corresponding metrics.

