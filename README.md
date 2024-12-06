## Ejercicio de clase

Iniciar entorno virtual
```
python -m venv .venv
source .venv/bin/activate
```

Freeze de dependencias
```
pip freeze > requirements.txt
```

Instalar dependencias
```
pip install -r requirements.txt
```

## Start server with gunicorn
```
gunicorn -b 0.0.0.0:8080 ejercicio_clase.wsgi:application
```

## Add hosts to ALLOWED_HOSTS
```
ALLOWED_HOSTS = ['*']
```

## install and configure whitenoise
```
pip install whitenoise
```
Configure whitenoise in settings.py
```
MIDDLEWARE = [
    'whitenoise.middleware.WhiteNoiseMiddleware',
    ...
]
```
