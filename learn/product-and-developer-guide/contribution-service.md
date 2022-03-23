# Contribution Service

The Contribution microservice enables organizations to digitally plan, coordinate and manage crowdsourcing of assets for defined projects.

Contribution service offers the APIs for creating and managing projects, their nominations, setting and reading user preferences, reading the configuration, getting the list of tenants and projects reports, etc. It stores information about the sourcing projects, their nominations, and configuration.

### API Documentation

To experience the APIs, please visit [here](http://docs.sunbird.org/latest/apis/programsapi/)

#### [Program APIs](http://docs.sunbird.org/latest/apis/programsapi/#tag/Program-CRUD)

[Program APIs](http://docs.sunbird.org/latest/apis/programsapi/#tag/Program-CRUD) provide the ability to organizations to create and manage projects to get the crowdsourcing of assets.

![](<../../.gitbook/assets/Program APIs (1).png>)

**Key features**

* [Create project](http://docs.sunbird.org/latest/apis/programsapi/#operation/CreateProgram200Success): This API creates the project to get the crowdsourcing of assets. Project by default is kept in draft mode and can be published later once the creator is ready to go live.&#x20;
* [Update project](http://docs.sunbird.org/latest/apis/programsapi/#operation/ProgramUpdate200Success): This API provides the ability to update the project details. For the published (Live) project only specific details are allowed to update e.g Project title, description, nomination and contribution dates.
* [Publish project](http://docs.sunbird.org/latest/apis/programsapi/#operation/Program-Publish200Success): The contribution organization or individual contributor can view and contribute the assets to only publish the project. This API enables the ability to publish the project.
* [Unlist publish project](http://docs.sunbird.org/latest/apis/programsapi/#operation/Unlist-Publish400BadRequest): This API provides control to get the contribution only from the organization that created the project.
* [Project list](http://docs.sunbird.org/latest/apis/programsapi/#operation/ProgramListsuccess-200): This API provides the list of projects available in a system. This API has the ability to apply filters.
* [List download](http://docs.sunbird.org/latest/apis/programsapi/#operation/ListDownload200Success): This API can be used to download the project details with insight full details like the number of nominations received, contribution received, sample received, contribution rejected, project metadata etc.
* [Read project](http://docs.sunbird.org/latest/apis/programsapi/#operation/Read-Program-200-Success): This API returns the entire project details.

#### [Nomination APIs](http://docs.sunbird.org/latest/apis/programsapi/#tag/Nomination)

[Nomination APIs](http://docs.sunbird.org/latest/apis/programsapi/#tag/Nomination) provide the ability to nominate and manage nominations made to the project.&#x20;

![](../../.gitbook/assets/nomination.png)

#### [Report API](http://docs.sunbird.org/latest/apis/programsapi/#tag/Report)

[Report API](http://docs.sunbird.org/latest/apis/programsapi/#tag/Report) generates the report of the approved asset contributed to the project.

#### [Configuration Search API](http://docs.sunbird.org/latest/apis/programsapi/#tag/Configuration)

[Configuration search API](http://docs.sunbird.org/latest/apis/programsapi/#tag/Configuration) supports searching the configuration by its key and status. The configuration entity provides the ability to mark configuration as active/ inactive. This configuration entity can be used to maintain a variety of configurations such as email/ SMS template configuration.&#x20;

#### [Tenant list ](http://docs.sunbird.org/latest/apis/programsapi/#tag/Tenant-list)

[Tenant list API](http://docs.sunbird.org/latest/apis/programsapi/#tag/Tenant-list) enables the ability to get a list of sourcing organizations that wants crowdsourcing of assets from the contributor for their projects. Tenant list API supports the filters, it can be used to get the active(live) / inactive tenant list.

#### ****[**Preference APIs**](http://docs.sunbird.org/latest/apis/programsapi/#tag/Preference)

[Preference APIs](http://docs.sunbird.org/latest/apis/programsapi/#tag/Preference) provide the ability to add, update, read user and project preferences.&#x20;

### Source Code

{% embed url="https://github.com/Sunbird-Ed/program-service" %}
