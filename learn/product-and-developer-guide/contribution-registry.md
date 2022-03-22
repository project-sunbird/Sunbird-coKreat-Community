# Contribution Registry

Contribution Registry is the single source of truth about all the contributors on co-kreat platform that nominate and contribute digital assets via sourcing projects. It stores the information about user, organization, role of the user in the organization. It also stores the mediums, classes and subjects user is contributing to. \
&#x20;\
When a person registers and logs in to Contribution Portal, the first thing he has to fill in is, whether he is an Individual contributor or an Contributing Organization. \


#### Contributing Organization&#x20;

When user enrolls as  a **Contributing Organization**, Contribution Registry stores the User, Org and User\_Org Schemas.  User gets added as a admin of that organization ( contribution org Admin), who later can invite other users to join his organization from contribution portal. These users can be called as Contributing Org Users.

A Contributing Org Admin can :\
&#x20;\-  Can nominate his organization for contributing to a project\
&#x20;\-  Can invite users to contribute to his projects\
&#x20;\-  Can assign contributors or reviewers to a project\
&#x20;\-  Can Review contributions done by contributors \
\
A user when uses invitation link shared by Contributing Org Admin, he becomes "User" of that specific organization. Admin can add these users as a contributor / Reviewer to the projects.\
\
A Contributor Org User can : \
&#x20; \- Can contribute / Review contents&#x20;

#### Individual Contributor

\
When a user enrolls as an **Individual Contributor**, only User schema is added in to Contribution Registry.&#x20;

An Individual Contributor can : \
&#x20;\- contribute the content by nominating to the respective project as an individual.\


![](../../.gitbook/assets/os\_search.png)

### API documentation

To experience the APIs, please visit [here](http://docs.sunbird.org/latest/apis/opensaber/)

### Schemas in the contribution Registry

#### User :

User schema stores the information about User.  If the user is an individual contributor this schema has roles column set as \["individual"], for contributor Org Admin it is set to \["admin"], for and for a contributing Org User it is set to \["User"]. It also adds up all the mediums, subjects, and classes a user is contributing to and update those values here.&#x20;

| Key          | Value                                               |
| ------------ | --------------------------------------------------- |
| @type        | <mark style="color:orange;">User</mark>             |
| userId       | user identifier from the diksha profile of the User |
| firstName    | firstname from the diksha profile of the User       |
| lastName     | lastName from the diksha profile of the User        |
| channel      | Channel from the diksha profile of the User         |
| enrolledDate | Date of enrollment                                  |
| osid         | Unique Id given to the User in the registry         |
| roles        | \[]                                                 |
| gradeLevel   | \[]                                                 |
| medium       | \[]                                                 |
| subject      | \[]                                                 |

#### Org :&#x20;

Org schema stores the information about Contributing Organization, which is given by contributing Org Admin while enrolling.&#x20;

| Key         | Value                                            |
| ----------- | ------------------------------------------------ |
| @type       | <mark style="color:orange;">Org</mark>           |
| name        | Name of the Organization                         |
| description | Description of the Organization                  |
| code        | code generated from the name of the Organization |
| osid        | Unique Id given to the Org in the registry       |
| orgId       |                                                  |
| type        |                                                  |

#### User\_Org :

User\_Org schema stores the mapping of the user and Contributing Organization. The roles param decide whether the user is a normal contributing user or the admin of the Organization.

| Key    | Value                                                                                                                            |
| ------ | -------------------------------------------------------------------------------------------------------------------------------- |
| @type  | User\_Org                                                                                                                        |
| orgId  | osid of the Org                                                                                                                  |
| userId | osid of the User                                                                                                                 |
| roles  | <p>role user belongs to in the Org. can be one or many from ["admin" , "user" , <br> "sourcing_admin", "sourcing_reviewer"] </p> |
| osid   | Unique Id given to the User\_Org mapping in the registry                                                                         |

### Source code

{% embed url="https://github.com/Sunbird-RC/open-saber" %}

####

\
