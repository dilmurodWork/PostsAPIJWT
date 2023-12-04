# JWT

1. JWT bilan ishlash uchun kerakli kutubxonani o'rnatamiz
```shell
pip install djangorestframework_simplejwt
```
2. `config/settings.py` ichida:
```python
INSTALLED_APPS = [
    'django.contrib.auth',
    ...,
    'rest_framework',
    'rest_framework.authtoken',
    'djoser',
    ...,
]
```
3. `config/urls.py`
```python
urlpatterns = [
    ...,
    url(r'^auth/', include('djoser.urls')),
    url(r'^auth/', include('djoser.urls.authtoken')),
]
```
4. 
```python
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework.authentication.TokenAuthentication',
        (...)
    ),
}
```
