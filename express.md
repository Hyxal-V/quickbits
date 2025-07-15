# Express.JS Quick Notes
## Basic Server Code

```js
const app = express();

// Define a port
const PORT = 3000;

// Basic route
app.get('/', (req, res) => {
  res.send('Hello, world!');
});

// Start the server
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
});
```
### Common Get Request
```js

app.get('/user', (req, res) => {
  const user = {
    id: 1,
    name: 'Hyxal',
    email: 'hyxal@example.com'
  };

  // Send JSON response
  res.json(user);
});
```
## Get Request
- Retrieve or `GET` data from the server.
```js
app.get(path,(request,response)=>{
    response.send()
})
```
### Route Parameters
```js
app.get('/user/:id', (req: Request, res: Response) => {
  const userId = req.params.id;
  res.send(`User ID is: ${userId}`);
});
```
### Query Parameters
```js

app.get('/search', (req, res) => {
  const term = req.query.term;
  const sort = req.query.sort;

  res.send(`Search term: ${term}, Sort by: ${sort}`);
});
```
## POST Request
-  Create send or `POST` data to the server
```js

app.post('/submit', (req, res) => {
  const data = req.body;
  console.log('Received data:', data);

  // Send a response back
  res.status(200).json({ message: 'Data received successfully', data });
});
```
## PUT Request
- `PUT` is used for replacing or updating existing resources.
```js

app.put('/user', (req, res) => {
  const userData = req.body;
  res.send(`User updated with name: ${userData.name}`);
});
```
