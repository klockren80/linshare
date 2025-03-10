/title RELEASE LinShare {VERSION}

# Validation tests

* [ ] Test manually a migration from the previous version with sample data
* [ ] Check if emails are enabled for the new features (fresh install/migration)
* [ ] Backport required changes from sql Patches (if exists) to Migration script
* [ ] Update [requirements](https://ci.linagora.com/linagora/lgs/linshare/products/linshare-github/-/blob/master/documentation/EN/installation/requirements.md) file

# Build and Perform Mvn release of each component

* [ ] core {VERSION}
* [ ] ui-user {VERSION}
* [ ] ui-admin {VERSION}
* [ ] ui-upload-request {VERSION}
* [ ] thunderbird {VERSION}

# Update all new versions in components Dockerfiles

* [ ] [linshare-ui-user-dockerfile](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-ui-user-dockerfile)
* [ ] [linshare-ui-upload-request-dockerfile](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-ui-upload-request-dockerfile)
* [ ] [linshare-ui-admin-dockerfile](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-ui-admin-dockerfile)
* [ ] [linshare-backend-dockerfile](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-backend-dockerfile)
* [ ] [linshare-database](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-database-dockerfile)
* [ ] [linshare-backend-documentation](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-backend-documentation-webservice-dockerfile)
* [ ] [linshare-init](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-init-dockerfile)

# Update linshare-github pom.xml

# Only for major or minor releases:

* [ ] IMPORTANT! : Change the version in /linshare-core/src/main/resources/sql/common/import-settings.sql
* [ ] Change LinShare version to new one in sql migration script
* [ ] Create a new upgrade file documentation

# Update the project CHANGELOG

* [ ] Backend changeLog
* [ ] User changeLog
* [ ] Upload request changeLog
* [ ] Admin ChangeLog
* [ ] Thunderbird plugin ChangeLog (optional)
* [ ] Screenshots
* [ ] Breaking changes


# [ ] Build and Perform Mvn release of release-linshare-suite

# [ ] Update docker-compose files:

* [ ] [linshare-docker](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-docker)
* [ ] [docker-compose.yml](https://ci.linagora.com/linagora/lgs/linshare/saas/linshare-docker-dev)

# Update demos

* official demo: demo.lisnhare.org
* sales team demo

# Communication

* [ ] Tweet the release with the new features. (With LinShare tweeter account)
