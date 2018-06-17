# filter-paginate-order-laravel

## usage example

<p>create a model</p>

```php
<?php

namespace App;

use App\BaseModel;

    class Article extends BaseModel
    {
        protected $guarded = [];

        protected $filter = [
            'id','title','content','author','created_at'
        ];

        public static function form(){
            return [
                'title'=>'',
                'author'=>'',
                'content'=>'',
                'small_content'=>'',
                'image'=>'',
                'is_active'=>true
            ];
        }
    }
```

<p>create a controller</p>

```php

  public function index()
  {
    return response()->json([
    'model'=>Article::filterPaginateOrder()
    ]);
  }

```
