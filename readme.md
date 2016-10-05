## Keycloak Provider for socialnorm

Custom provider for https://github.com/adamwathan/eloquent-oauth-l5

just add irisit/socialnorm-keycloak to your main install 

More doc in comming, do no hesitate to contact me for more info or help !

```php
// config/eloquent-oauth.php
return [
    'model' => User::class,
    'table' => 'oauth_identities',
    'providers' => [
        'facebook' => [ /* ... */],
        'google' => [ /* ... */],
        'keycloak' => [
            'client_id' => 'xxxxxxx',
            'client_secret' => 'xxxxxxxx',
            'redirect_uri' => 'http://localhost.dev/keycloak/callback',
            'scope' => [],
            'auth_server' => 'http://keycloak.dev/auth',
            'auth_realm' => 'mygreatrealm',
        ],
    ],
];