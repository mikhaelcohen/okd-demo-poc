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

## PaaS Deployement

### Create app
```
oc new-app https://github.com/mikhaelcohen/okd-demo-poc
```

### Create Route
```
oc create route --service=okd-demo-poc --hostname=web.pocokd.cloudwatt.com
```

## CaaS Deployement

### DB Deployement

```
oc process mongodb-ephemeral -p MONGODB_USER=letschatUser -p MONGODB_PASSWORD=letschatPass -p MONGODB_DATABASE=letschat -p MONGODB_ADMIN_PASSWORD=admin -n openshift | oc apply -f -
```

### App Deployement

```
oc apply -f letschat-dc.yml
```
