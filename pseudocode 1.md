
# Workflow Pseudocode
 
## 1.Project API

### 1.1 Function to add a new project

- Method: POST
- API End Point: `/project`
- Request: `req.body`
- Response: `res.status(200).json({ data: newProject })`

    1. when the user hits the `/project` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 1.2 Function to update an existing project based on id.

- Method: PUT
- API End Point: `/project/{id}`
- Request: `req.params.id`
- Response: `res.status(200).json({ data: newProject })`

    1. when the user hits the `/project/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 1.3 Function to delete a project based on id.

- Method: DELETE
- API End Point: `/project/{id}`
- Request: `req.params.id`
- Response: `res.status(200).json({ message: 'Stage deleted successfully' });`

    1. when the user hits the `/project/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 1.4 Function to get list of all projects 

- Method: GET
- API End Point: `/project`
- Request: async `(req, res)`
- Response: `res.status(200).json(project)`

    1. when the user hits the `/project/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 1.5 Function to get an existing project basedon id.

- Method: GET
- API End Point: `/project/{id}`
- Request: async `(req, res)`
- Response: `res.status(200).json(project)`

    1. when the user hits the `/project/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

## 2.Stage Management API

### 2.1Add a New Stage

- Method: POST
- API End Point: `/project/{id}/stages`
- Request: `req.body`
- Response: `res.status(201).json({ data: newStage })`

    1. when the user hits the `/usecase/{usecaseId}/stage` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation
### 2.2 Get a Stage by ID

- Method: GET
- API End Point: `  /project/{projectid}/stage/{id}`
- Request: async `(req, res)`
- Response: `res.status(200).json(stageId);`

    1. when the user hits the ` /usecase/{usecaseId}/stage/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 2.3 Update an Existing Stage based on id

- Method: PUT
- API End Point: ` /project/{projectid}/stage/{id}`
- Request: `req.params.id`
- Response: `res.status(200).json({ data: newStage })`

    1. when the user hits the ` /usecase/{usecaseId}/stage/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 2.4 Delete a Stage by id

- Method: DELETE
- API End Point: ` /project/{projectid}/stage/{id}`
- Request: `req.params.id`
- Response: `res.status(200).json({ message: 'Stage deleted successfully' });`

    1. when the user hits the ` /usecase/{usecaseId}/stage/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation

### 2.5 Function to list stages in particular project

- Method: GET
- API End Point: `/project/{id}/stages`
- Request: async `(req, res)`
- Response: `res.status(200).json(stages)`

    1. when the user hits the `/project/{id}/stages` endpoint an event is started.
    2. this event triggers the correponding lambda with the request.
    3. lambda communicates with the postgresql database and performs the related crud operation
