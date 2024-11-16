This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).


Proyecto: Sistema de Tipo de Cambio - Backend


______________________________________________________________________
Descripción
Este es el backend del Sistema de Tipo de Cambio, desarrollado con Spring Boot. Proporciona una API para consultar el tipo de cambio actual y su historial.

Tecnologías Utilizadas
Framework: Spring Boot
Base de Datos: MySQL
Conexión a SOAP: Servicio SOAP de Banguat para obtener el tipo de cambio.




___________________________________________________________________________
Requisitos Previos
Java 17: Versión recomendada.
Maven: Administrador de dependencias.
MySQL: Para la base de datos.
Instalación y Configuración
Clona el repositorio:

bash
Copiar código
git clone <URL_DEL_REPOSITORIO>
cd backend
Configura la base de datos:

Crea una base de datos en MySQL con el nombre tipo_cambio.
Actualiza src/main/resources/application.properties con tus credenciales:
properties
Copiar código
spring.datasource.url=jdbc:mysql://localhost:3306/tipo_cambio
spring.datasource.username=TU_USUARIO
spring.datasource.password=TU_CONTRASEÑA
Compila e instala las dependencias:

bash
Copiar código
mvn clean install
Inicia la aplicación:

bash
Copiar código
mvn spring-boot:run
Accede a las APIs en http://localhost:8080.

Endpoints Principales
Obtener Tipo de Cambio Actual:

Método: GET
Ruta: /api/tipo-cambio/actual
Respuesta:
json
Copiar código
{
  "fecha": "2024-11-16",
  "tipoCambio": 7.85
}
Obtener Historial de Tipos de Cambio:

Método: GET
Ruta: /api/tipo-cambio/historial
Respuesta:
json
Copiar código
[
  { "fecha": "2024-11-15", "tipoCambio": 7.84 },
  { "fecha": "2024-11-14", "tipoCambio": 7.83 }
]






___________________________________________________________________________-

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
