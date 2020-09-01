### Week 4

***

#### Class 16

##### Review, Research, Discussion
* Why is access control important?
  * We don't want to give every user who logs in the same capabilities. For example, some users would have administrative privileges, others would have the ability to edit content, and some would simply have read-only access.
* Describe an application that would need access control.
  * Blogs or other Publications, Government Agencies, Financial Institutions
  * Essentially anything with potentially sensitive information attached
* What is a role used for?
  * To define a user's capabilities as they relate to data within an application
* Why is role based access control more scalable than discretionary or mandatory access control?
  * Mandatory Access Control is strictly enforced by one system administrator and requires a great deal of planning before implementation; there is also a high system management overhead associated with constantly updating object and account labels, as these things must change to accomodate new data and new users, as well as changes to categories and classification of existing users. As the user base grows, this practice becomes less scalable because of the high level of autonomy each user has over its own data.
  * Discretionary Access Control is enforced by the operating system (under control of a system administrator). It is categorized by the user's ability to control access to their own data. 
  * Role Based Access Control assigns permissions to particular roles within an organization. Users, upon signup, are assigned to that particular role. This is the most scalable because there are no deviations from this rule. One user will never have more capabilities than another user, and one editor will never have more capabilities than another editor. By creating roles first, it is ensured that no matter how many users of any type are added, their permissions are granted in the same way and there don't need to be changes to the code.
