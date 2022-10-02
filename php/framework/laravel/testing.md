# Testing

## Testing facades

If you use the facades inside the code, you can mock it like the following example:

```php
<?php

namespace App\Service;

use Illuminate\Support\Facades\Log;
use Illuminate\Support\Facades\File;

class MyService
{
    function checkFile($Path)
    {
        if(File::exists($Path))
            return true;
            
        Log::info("Not found file: ".$Path);
        return false;
    }
}

```

```php

namespace Tests\Unit;
 
use PHPUnit\Framework\TestCase;
use App\Service\MyService;

use Illuminate\Support\Facades\Log;
use Illuminate\Support\Facades\File;
 
class ExampleTest extends TestCase
{

    public function test_checkFile_notExist()
    {
        File::shouldReceive('exists')->once()->andReturn('false');
        Log::spy();

        $myService = new MyService();
        $this->assertFalse($myService->checkFile("Test.txt"));

        Log::shouldHaveReceived('info')->once()->with("Not found file: Test.txt");
    }


    public function test_checkFile_exist()
    {
        File::shouldReceive('exists')->once()->andReturn('false');

        $myService = new MyService();
        $this->assertTrue($myService->checkFile("Test.txt"));

    }
}

```

Official documentation: [Mocking facades](https://laravel.com/docs/9.x/mocking#mocking-facades)