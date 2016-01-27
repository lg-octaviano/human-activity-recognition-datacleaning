## Transformations made to the dataset
For both the train and test datasets, the feature vector was imported and linked with the activity name (walking, sitting, etc.) and subject ID (the identifier for the person who did the activity).
The two datasets were then merged together into a single one.
We then filtered the columns to select only the columns that contained the mean and standard deviation calculations of the measurements.
The columns were then renamed and a final data set was generated containing the mean for all the columns, grouped by activity name and subject id.

## Variables in the final data set
Activity.Name
	- Name of the activity being performed by subject
	- Values: LAYING, SITTING, STANDING, WALKING, WALKING_DOWNSTAIRS, WALKING_UPSTAIRS

Subject.id
	- Number identifier for the person performing the activity
	- Values: [1, 30]

The other variables are means (over subject and activity) for several measurements.
The measurements are identified in the variable names follows:
	[Domain].[PhysicalQuantity].[Aggregation].[Axis] where:
	Domain can be TimeDomain or FrequencyDomain, meaning the measurement was calculated in the time domain or frequency domain respectively.
	PhysycalQuantity can be BodyAcceleration, GravityAcceleration, BodyAcceleration.Jerk, BodyAngularVelocity or BodyAngularVelocity.Jerk.
	Aggregation can be mean or std, meaning mean and standard deviation calculated over time.
	Axis can be X, Y or Z, denoting the three axis in three-dimensional space.
The measurements were normalized in the range of [-1, 1].