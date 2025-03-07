---
title: Raven Credentials
description: Credentials - Raven
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import useBaseUrl from '@docusaurus/useBaseUrl';

[1]: #get-the-raven-credentials
[2]: #create-a-raven-credentials
[3]: #delete-raven-credentials

Form of a Raven Credentials resource:

```json
{
  "accessToken": "str",
  "refreshToken": "str",
  "clientId": "str",
  "clientSecret": "str",
  "status": "str" 
}
```


**Endpoints**

Description | Endpoints
--- | ---
[Get the Raven credentials][1] | <span class="badge badge--success">GET</span> `/users/{leafUserId}/raven-credentials`
[Create a Raven credentials][2] | <span class="badge badge--warning">POST</span> `/users/{leafUserId}/raven-credentials`
[Delete Raven credentials][3] | <span class="badge badge--danger">DELETE</span> `/users/{leafUserId}/raven-credentials`


## Raven Credentials Endpoints

### Get the Raven credentials
&nbsp<span class="badge badge--success">GET</span> `/users/{leafUserId}/raven-credentials`  
Get the Raven credentials of the Leaf User based on its `id` and returns a JSON with the credentials.

#### Response
A Raven credentials resource as a JSON.

#### Request examples

<Tabs
  defaultValue="sh"
  values={[
    { label: 'cURL', value: 'sh', },
    { label: 'Python', value: 'py', },
    { label: 'JavaScript', value: 'js', },
  ]
}>
  <TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  axios.get(endpoint, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  response = requests.get(endpoint, headers=headers)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
  curl -X GET \
      -H 'Authorization: Bearer YOUR_TOKEN' \
      'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  ```

  </TabItem>
</Tabs>


### Create a Raven credentials
&nbsp<span class="badge badge--warning">POST</span> `/users/{leafUserId}/raven-credentials`  

Create a Raven credentials for the Leaf User.

#### Request examples
A Raven credentials.

```json
{
  "clientId": "str",
  "clientSecret": "str",
  "refreshToken": "str"
}
```

<Tabs
  defaultValue="sh"
  values={[
    { label: 'cURL', value: 'sh', },
    { label: 'Python', value: 'py', },
    { label: 'JavaScript', value: 'js', },
  ]
}>
  <TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  const data = {
    "clientId": "str",
    "clientSecret": "str",
    "refreshToken": "str"
  }

  axios.post(endpoint, data, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  data = {
    "clientId": "str",
    "clientSecret": "str",
    "refreshToken": "str"
  }

  response = requests.post(endpoint, headers=headers, json=data)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
curl -X POST \
-H 'Authorization: Bearer YOUR_TOKEN' \
-H 'Content-Type: application/json' \
-d '{ "clientId": "str","clientSecret": "str","refreshToken":"str"}' \
'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  ```

  </TabItem>
</Tabs>

#### Response
A Raven Credentials with status.


### Delete Raven credentials
&nbsp<span class="badge badge--danger">DELETE</span> `/users/{leafUserId}/raven-credentials`  

Delete Leaf User's Raven credentials.

#### Request examples
<Tabs
  defaultValue="sh"
  values={[
    { label: 'cURL', value: 'sh', },
    { label: 'Python', value: 'py', },
    { label: 'JavaScript', value: 'js', },
  ]
}>
  <TabItem value="js">

  ```js
  const axios = require('axios')
  const TOKEN = 'YOUR_TOKEN'

  const endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  const headers = { 'Authorization': `Bearer ${TOKEN}` }

  axios.delete(endpoint, { headers })
      .then(res => console.log(res.data))
      .catch(console.error)
  ```

  </TabItem>
  <TabItem value="py">

  ```py
  import requests

  TOKEN = 'YOUR_TOKEN'

  endpoint = 'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  headers = {'Authorization': f'Bearer {TOKEN}'}

  response = requests.delete(endpoint, headers=headers)
  print(response.json())
  ```

  </TabItem>
  <TabItem value="sh">

  ```shell
  curl -X DELETE \
      -H 'Authorization: Bearer YOUR_TOKEN' \
      'https://api.withleaf.io/services/usermanagement/api/users/{leafUserId}/raven-credentials'
  ```

  </TabItem>
</Tabs>
