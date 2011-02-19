Users:
  GET 'api/v0/users/:user_uuid'
  GET 'api/v0/users'
  POST 'api/v0/users/'
  PUT 'api/v0/users/:user_uuid'
  DELETE 'api/v0/users/:user_uuid'
    - Probably not used by the app, but necessary for any admin dashboard we put on this.
  POST 'api/v0/users/:user_uuid/sessions'
    - Checks the validity of a user id and password.

Tasks and lists will have operations similar to the first four above.

  GET 'api/v0/lists/:list_uuid/tasks'
    - Retrieves a list of tasks for a list.

  GET 'api/v0/lists'
    - Returns a list of all of the user's lists.

  GET 'api/v0/tasks'
    - Returns a list of all of the user's tasks.

Tasks in a shared list are not themselves modifiable, unless a lock is active on the list. 

The List sharing and locking  methods are:
  PUT 'api/v0/lists/:list_uuid/lock'
  PUT 'api/v0/lists/:list_uuid/unlock'
  PUT 'api/v0/lists/:list_uuid/share'
    - The only parameter is the user to share it with.
  PUT 'api/v0/lists/:list_uuid/unshare'
    - The only parameter is the user to unshare share it with.

TODO:
  Think about API methods to enable retrieving subsets of tasks, based on reasonable criteria.
