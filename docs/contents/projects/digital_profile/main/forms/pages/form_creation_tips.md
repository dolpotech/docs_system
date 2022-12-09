##Tips on creating forms:

Always give the value of select options in text format instead of integer or decimal format.
If there are any set of fields that are to be repeated, make sure that they are grouped together.

Also, any information related to the fields to be repeated should be included in the same group. This is to make sure that every repeating groups in a form are independent from each other.

**Repeating groups**

When creating repeating groups, there might be some cases where we would not want to include every repeated data for a question. So, for this purpose, appending “__R” to the last of question value(you can set this by clicking the settings icon on the question) would denote that all the answers to this question can be used in reporting. Similarly, not attaching “__R” would denote that only one answer to this question will be used in reporting.

**Unique values**
Every values in the select option should be textual format rather than integer or decimal format and each and every option value’s or question’s name should be unique throughout the form.


# getting koboforms form edit url using dashboard system
step1: get form id_string from ReadOnlyKobocatXform

Step2: get id from form submission instance id

step3: form the url of following pattern

id_string =a6KsgAxLV5M3SNsrV3M78D

instance_id =364

http://digitalprofile.qbitsx.com/en/edit-data/a6KsgAxLV5M3SNsrV3M78D/364