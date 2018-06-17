# filter-paginate-order-laravel

## usage example

#### model
```php
<?php

namespace App;

use Illuminate\Database\Eloquent\Model;

class Article extends Model
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

#### controller

```php

  public function index()
  {
    return response()->json([
    'model'=>Article::filterPaginateOrder()
    ]);
  }

```
