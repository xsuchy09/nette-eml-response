# nette-eml-response
EmlResponse for Nette.

## Install
```composer
composer require xsuchy09/nette-eml-response
```

## Usage
```php
class SomePresenter extends BasePresenter
{
	public function actionDefault()
	{
		$emlData = file_get_contents('mail.eml');

		$response = new \xsuchy09\Application\Responses\EmlResponse($emlData, 'download.eml');
		$this->sendResponse($response);
	}
}
```