# Basic Express Site (2016 Edition)

A simple website in node js to accompany a blog post.

## Setup

```
npm i
npm run build
npm start

# development mode (watches for source changes)
npm run watch
```

## Screenshot

![Screenshot](https://raw.githubusercontent.com/bengourley/basic-express-site-2016/master/screenshot.png)


## Creation DB
oc process mongodb-ephemeral -p MONGODB_USER=userMongo -p MONGODB_PASSWORD=passMongo -p MONGODB_DATABASE=todo -p MONGODB_ADMIN_PASSWORD=admin -n openshift | oc apply -f -

## Creation app
oc new-app https://github.com/mikhaelcohen/okd-demo-poc
