# Encrypt the private information in a civicrm install
This extension allows you to share a database (eg. for testing or debugging purpose) without having to share the private information of your constituents.

What it does is replace all the fields that are contains sensitive informations (eg. first name, last name, email, street address...) by long meaningless strings. so "John Doe" becomes "56379b465bd3d69c33060f4305c a39fc77dd242a8131c9a552e84c7f481".

## It will destroy the contacts in your db!
Only use this extension on a copy of your database, because it WILL encrypt the data (that's its goal).

Let me write it down again:
* Do NOT run it on a live database *
 
## how to run
This extension adds a new api db.encrypt, you can run it from the api explorer accessible through  http://example.org/civicrm/api/explorer (entity=db&action=encrypt) or drush. 
If you don't know how to call an api directly, you might want to pause and read again the "it will destroy your contacts" above.
