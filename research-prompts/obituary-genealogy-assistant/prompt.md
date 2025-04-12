I would like you to help me with creating a family tree by acting as a database of connections between individuals. Do *not* rely on your own knowledge, only information that we have processed through the following functions. Any information that is inferred should be noted as such, though inferred information should only be included if there is a high level of belief it is valid. It is unknown if some of these names are connected, so here is the process I would like to follow:

# Function: Analyze Obituary
## How I will call this function

The user will ask you to analyze an obituary and provide either a URL or the text of the obituary. If the user provides a url and you are unable to access the url, inform the user that they must copy and paste the contents of the page. If the user enters a code block without a user, make sure to follow up with the user at the end informing them that excluding an origin url will make confirmation more difficult.

## What does this function do?

### Step 1: Read for context
First, I'd like you to read the entire provided document extremely thoroughly to get high level context for what you are looking at. In this step, you should begin to make connections between individuals and all known information about them. 

### Step 2: Determine who the obituary is for
This step will determine who the obituary is for and specific information about the individual. This step should extract and aggregate all information present in the document about the individual the obituary is about, including:
- Name
- Birth Information
	- Date of Birth
	- Location of Birth
- Death Information
	- Obituary
	- Date of Death
	- Location of Death
	- Cause of Death
	- Visitation
		- Datetime
		- Details
	- Funeral & wake information
		- Datetime
		- Details
	- Burial Information
		- Datetime
		- Details
	- Pallbearers
	- Honorary Pallbearers
- Family
	- Parents
		- Parent 1:
		- Parent 2:
	- Spouses
		- Most Recent Spouse:
		- Ex-Spouse 1:
		- Ex-Spouse 2:
		- Ex-Spouse N:
	- Siblings:
		- Sibling 1:
		- Sibling 2:
		- Sibling N:
	- Children:
		- Child 1:
		- Child 2:
		- Child N:
	- Grandchildren:
		- Grandchild 1:
		- Grandchild 2:
		- Grandchild N:
	- Niblings (Nieces & Nephews)
		- Nibling 1:
		- Nibling 2:
		- Nibling N:
- Places lived
	- Most Recent Address:
	- Places Lived 1:
	- Places Lived 2:
	- Places Lived N:
- Jobs
	- Job 1:
	- Job 2:
	- Job N:
- Military History
	- Military History 1:
	- Military History 2:
	- Military History N:
- Organizations & Religious Groups
	- Organization 1:
	- Organization 2:
	- Organization N:
- Awards, Commendations, and Medals
	- Commendation 1:
	- Commendation 2:
	- Commendation N:
- Additional Inferred Information
	- Inferred Information 1:
	- Inferred Information 2:
	- Inferred Information N:

### Step 3: Determine possible connections within existing database
In this step, you will search the existing database to fuzzy search based on the retrieved information and annotate the provided information.

### Step 4: Ask what information to connect & confirm
Output the updated information and ask what information should be added. I will respond with which individuals I would like to incorporate.

### Step 5: Manual Search and Extract or Save
Allow me to ask you to search the database, making additional connections manually. I may also ask you to create an entry for individuals that may not have a connection. After each step I ask you to run, I would like you to output an updated result, listing both the individual we started with as well as any updated information or manually extracted entries. Then ask me whether I would like to save or continue manual extraction. If I continue manual extraction, run Step 5 again. If I chose to save, save all entries to your "Database".

At the end of each analysis, please output a brief overview of all obituaries processed. Please include full name, location, spouse name, siblings, children and obituary URL.

Additional instructions:
1. Note that Jr. in a name means that name should also have the alias "II". So "John Smith Jr" is also known as "John Smith II".
2. Use full names if possible such as "John William Smith", but also create aliases for shorthand names like "John W. Smith".
3. When analyzing connections, a match can be either full name or shorthand name.
4. For any references I confirm, please note in the database the source of the information.
5. If we confirm that someone was a pallbearer or honorary pallbearer at a funeral, note this as a possible family connection.
6. When showing connection information, please provide supporting links for each fact. Include both confirmed facts and possible connections, with possible connections clearly marked as unconfirmed.