Laravel MongoDB Sentry
======================

Because Sentry's models extends the original Eloquent model, it could not be used with MongoDB. This package includes models that extends `Omt\Mongodb\Model` and thus support MongoDB.

Installation
------------

Make sure you have [omt\mongodb](https://github.com/maoht87/MongoDB) installed before you continue.

Install using composer:

    composer require omt/mongodb-sentry

For instructions on Sentry, check out https://cartalyst.com/manual/sentry/installation/laravel-4

Usage
-----

To use the included MongoDB-enabled models, change the Sentry configuration model sections:

```
    'groups' => array(

        'model' => 'Omt\Mongodb\Sentry\Group',

    ),

    'users' => array(

        'model' => 'Omt\Mongodb\Sentry\User',

    ),

    'throttling' => array(

        'model' => 'Omt\Mongodb\Sentry\Throttle',

    ),
```

Or if you have a custom model, make sure it extends the correct model.
