# Challenge Técnico Fullstack

El objetivo es construir una solución simple para gestionar solicitudes de seguros llamadas **Requests**.

Una Request tiene la siguiente estructura:

```ts
type Request = {
  id: string;
  code: string;
  category: "FIRE" | "LIFE" | "CAR";
  createdAt: string;
  status: "PENDING" | "PROCESSED" | "REJECTED";
};
```

***

## Frontend – React + TypeScript

Crear una aplicación que permita:

* Listar Requests
* Crear una nueva Request
* Cambiar el estado de una Request de `PENDING` a `PROCESSED` o `REJECTED`

Requisitos:

* React
* TypeScript
* Consumo de API REST
* UI simple y clara

***

## Backend – Node.js + TypeScript

Crear una API REST que permita:

* Crear Requests
* Listar Requests
* Obtener una Request por `id`
* Cambiar el estado de una Request
* Eliminar una Request

Reglas:

* Toda Request nueva debe crearse con estado `PENDING`
* `createdAt` debe asignarse automáticamente
* Solo se puede cambiar el estado desde `PENDING` hacia `PROCESSED` o `REJECTED`

Endpoints sugeridos:

```http
GET /requests
GET /requests/:id
POST /requests
PATCH /requests/:id/status
DELETE /requests/:id
```

***

## Se evaluará

* Código claro y ordenado
* Buen uso de TypeScript
* Manejo de errores
* Validaciones básicas
* Organización del proyecto
* Instrucciones claras para ejecutar

***

## Bonus opcional

* Tests
* React Query
* React Hook Form
* Swagger
* Docker
* Base de datos real

***

Mi recomendación: **sacaría Claim del alcance principal** y lo dejaría como bonus.  
Así el challenge sigue evaluando lo mismo, pero queda mucho más enfocado y menos intimidante.
