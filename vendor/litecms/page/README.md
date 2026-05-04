Lavalite package that provides page management facility for the cms.

## Installation

Run the below command form the root folder of lavalite.

```
    composer require "litecms/page"
```


## Migration and seeds

```
    php artisan migrate
    php artisan db:seed --class=Litecms\\Page\\Seeders\\PageTableSeeder
```

## Publishing

* Configuration
```
    php artisan vendor:publish --provider="Litecms\Page\Providers\PageServiceProvider" --tag="config"
```
* Language
```
    php artisan vendor:publish --provider="Litecms\Page\Providers\PageServiceProvider" --tag="lang"
```
* Views
```
    php artisan vendor:publish --provider="Litecms\Page\Providers\PageServiceProvider" --tag="view"
```


## URLs and APIs


### Web Urls

* Admin
```
    http://path-to-route-folder/admin/page/{modulename}
```

* User
```
    http://path-to-route-folder/user/page/{modulename}
```

* Public
```
    http://path-to-route-folder/pages
```


### API endpoints

These endpoints can be used with or without `/api/`
And also the user can be varied depend on the type of users, eg user, client, admin etc.

#### Resource

* List
```
    http://path-to-route-folder/api/user/page/{modulename}
    METHOD: GET
```

* Create
```
    http://path-to-route-folder/api/user/page/{modulename}
    METHOD: POST
```

* Edit
```
    http://path-to-route-folder/api/user/page/{modulename}/{id}
    METHOD: PUT
```

* Delete
```
    http://path-to-route-folder/api/user/page/{modulename}/{id}
    METHOD: DELETE
```

#### Public

* List
```
    http://path-to-route-folder/api/page/{modulename}
    METHOD: GET
```

* Single Item
```
    http://path-to-route-folder/api/page/{modulename}/{slug}
    METHOD: GET
```

#### Others

* Report
```
    http://path-to-route-folder/api/user/page/{modulename}/report/{report}
    METHOD: GET
```

* Export/Import
```
    http://path-to-route-folder/api/user/page/{modulename}/exim/{exim}
    METHOD: POST
```

* Action
```
    http://path-to-route-folder/api/user/page/{modulename}/action/{id}/{action}
    METHOD: PATCH
```

* Actions
```
    http://path-to-route-folder/api/user/page/{modulename}/actions/{action}
    METHOD: PATCH
```

* Workflow
```
    http://path-to-route-folder/api/user/page/{modulename}/workflow/{id}/{transition}
    METHOD: PATCH
```
