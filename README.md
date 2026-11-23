# Modelos del e-commerce

Modelos de Django para un e-commerce, separados en apps: productos, carrito, pedidos, direcciones y perfiles de facturación. Forma parte de la serie de tareas del proyecto e-commerce de la profesión Full Stack Python de EBAC. Cada repositorio guarda el proyecto como quedó al terminar ese tema; la versión final es [e-commerce-completo](https://github.com/Moremaster123/e-commerce-completo).

## Tecnologías

- Python y Django 6.1
- SQLite

## Apps y modelos

| App | Modelo | Relación |
|---|---|---|
| `product` | `Product` | nombre, descripción y precio |
| `cart` | `Cart` | pertenece a un usuario y tiene muchos productos (ManyToMany) |
| `order_manager` | `Order` | uno a uno con un carrito; guarda el total y la fecha |
| `address` | `Address` | calle, ciudad, estado, país y código postal |
| `billing_profile` | `BillingProfile` | une a un usuario con una dirección |

## Cómo ejecutarlo

```bash
python -m venv venv
venv\Scripts\activate        # en Linux o macOS: source venv/bin/activate
pip install django
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Después entra a `http://127.0.0.1:8000/admin/`.

## Autor

Juan Carlos González Herrera · [LinkedIn](https://www.linkedin.com/in/juan-carlos-desarrollador-web) · [Portafolio](https://moremaster123.github.io)
