## Starter Pack for a react/redux/apollo-client application for easy project generation.

### inludes:
- authentication,
- error tracking (Sentry)
- Testing (Jest+Enzyme)
- Custom components library.
- Google Analytics.


## Getting Started

1. `git clone `
2. Add the following secrets to .env file:
```
REACT_APP_ENV= 'dev' or 'production'
REACT_APP_PRODUCTION = true
REACT_APP_AUTH0_CLIENT_ID='XXXX' //from auth0 console
REACT_APP_AUTH0_DOMAIN='XXXX' //from auth0 console
REACT_APP_DEV_ROUTE='XXXX' //to view development only routes. i.e) mockup of
app layout is available for developers that know this secret
REACT_APP_GRAPHCOOL_ENDPOINT='wss://XXXX' //use dev api in development
REACT_APP_GRAPHCOOL_WSS_ENDPOINT='https://XXXX' //use dev api wss in development.
REACT_APP_GRAPHCOOL_FILE_ENDPOINT='https://XXXX' //use dev api wss in development.
REACT_APP_SENTRY_URL='https://XXXX'
REACT_APP_GOOGLE_ANALYTICS_ID='UA=XXXX'
NODE_PATH = 'src' //to enable absolute imports
```

 3. install dependencies `npm install`
 4. Change name in package.json, index.html, and add own logo.

**Make sure env variables set in production ( i.e: heroku Config Vars )

## Built With

* React
* Redux
* Apollo client
* create react app
* Sentry
* Heroku
* Auth0/ Auth0 lock

## Documentation

* check out `./docs` for more project specifics.
* check out `CREATE_REACT_APP_README.md` for any create-react-app stuff.

## Project structure overview:
Top level component that contains the app: `components/App.js`

1. All GraphQL operations (queries, mutations, subscriptions) in `gql/` directory.
2. All custom easily reusable ui components in `ui-kit/`
3. All other components in `components/` directory. Data fetching components
(Components with Apollo gql queries) names end in `Container`. ** Don't confuse
with redux style Container-Component project structure. Other components may
still be connected to redux and Apollo (i.e so don't have to pass mutations down
multiple levels), but they are not primary data fetching components.
4. Global style related files are in `styles/` directory
( animations, colors, z-Index ...)
5. Redux store split into Apollo and App. App contains all non-apollo related.
state.
6. Redux files - Action creators in `actions/` reducers in `reducers`
