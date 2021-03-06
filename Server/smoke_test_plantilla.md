# Smoke test

## Previous requirements

Prepare two servers with ssl activated and trusted certificates.

Enable LDAP and external storage apps.

Have a LDAP server ready to be used with owncloud.

Have ready two external storages of your choice SMB, SFTP, Dropbox, Google Drive, FTP, S3, ownCloud, local.

## Testing setup


TestID | Test Case | Expected Result | Result | Related Comment
------------ | ------------- | -------------- | ----- | ------
1 | Enable encryption app and encryption default module | Encryption is enable correctly | [ ] |
2 | Populate owncloud server with users and groups | Users and groups are correctly created | [ ] |
3 | Share a folder remotely using federated sharing with admin user of the other server. | folder can be opened in recipient server without problems | [ ] |
4 | Set up LDAP, as admin check users. log in with a LDAP user, if possible one with an avatar. | Users are loaded. LDAP user logs in without problems. Avatar is shown if exist.  | [ ] |
5 | Set up two external storages different, disable encryption in one of them.| No errors in this process | [ ] |

##Testing functionality

TestID | Test Case | Expected Result | Result | Related Comment
------------ | ------------- | -------------- | ----- | ------
1 | Share a file using federated sharing from an external unencrypted external storage in server #1 using LDAP user  to the admin user in server #2. | Admin user in server #2 can see the file. | [ ] |
2 | Open internet explorer or edge and upload a new avatar for a regular user not LDAP | Interface can be used, avatar is uploaded, check that personal page has a scroll bar and scrolls fine. | [ ] |
3 | Upload several files and folder inside external storages, open some. | No problems uploading, files can be downloaded and open. | [ ] |
4 | Delete files inside both external storages. Recover some after in the trashbin. |  Files are correclty deleted and restored. | [ ] |
5 | Using webdav upload a 100MiB file.| No errors in this process | [ ] |


Pyocclient status:

- Travis stable8		![stable8 pyocclient] (https://travis-ci.org/owncloud/pyocclient.svg?branch=stable8)
- Travis stable8.1 	![stable8.1 pyocclient] (https://travis-ci.org/owncloud/pyocclient.svg?branch=stable8.1)
- Travis stable8.2 	![stable8.2 pyocclient] (https://travis-ci.org/owncloud/pyocclient.svg?branch=stable8.2)
- Travis master 		![master pyocclient] (https://travis-ci.org/owncloud/pyocclient.svg?branch=master)


Smashbox status:

Git master: [![Build Status](https://ci.owncloud.org/job/smashbox-on-docker-daily-master/badge/icon)](https://ci.owncloud.org/job/smashbox-on-docker-daily-master/)
