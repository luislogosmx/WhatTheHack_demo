# Reto 01 - Configura tu entorno de desarrollo

[< Reto Anterior](./Challenge-00.md) - **[Home](../README.md)** - [Siguiente reto >](./Challenge-02.md)

## Introducción

Con la copia del proyecto obtenida, es momento de centrar tu atención en configurar tu entorno de desarrollo. El refugio está interesado en asegurar que los desarrolladores puedan contribuir al proyecto de la manera más fluida posible, evitando configuraciones tediosas. Para cumplir con este requisito, configurar el proyecto de manera local no es la mejor opción. Deberás buscar una solución basada en la nube que permita un entorno de desarrollo configurado de manera centralizada 😉.

## Descripción

Crearás un entorno de desarrollo que cumpla con las necesidades mencionadas anteriormente. Quieres poder comenzar a escribir código sin necesidad de instalar recursos localmente en tu máquina.

GitHub Codespaces es un entorno de desarrollo en la nube que nos ayudará a trabajar sin necesidad de instalar nada localmente en tu máquina, todo se hará en la nube. Aquí puedes ver más sobre lo que es un [GitHub Codespace](https://docs.github.com/es/codespaces/overview).

Durante el desarrollo (en un reto posterior), crearás recursos en Azure y configurarás tu repositorio en GitHub utilizando GitHub Actions, Azure CLI y GitHub CLI. No es necesario que crees recursos en Azure directamente, ya que hemos preparado scripts que lo harán por ti. Solo necesitarás seguir las instrucciones y asegurarte de que todo esté correctamente configurado en tu repositorio de GitHub.

Al inicio del taller, recibirás los detalles necesarios para acceder a la cuenta de Azure. Asegúrate de iniciar sesión en Azure desde una ventana de incógnito y selecciona la opción para habilitar la seguridad más tarde. Estas cuentas de Azure se han creado solo para este reto y serán eliminadas al final, por lo que no te preocupes por habilitar la seguridad ahora. Repetimos, sin embargo, que en este reto de configuración NO crearás recursos de Azure, pues esto se realizará más adelante. De momento, considera esto solo como información complementaria.

La aplicación utiliza una variable de entorno llamada **MONGODB_URI** con el valor **mongodb://localhost** para conectarse a la base de datos MongoDB. Puedes agregar esta variable en los settings de tu repositorio, en la sección de Codespaces, como un secreto cifrado.

En primer lugar, crea un Codespace a partir del repositorio que se encuentra en tu cuenta de GitHub. Una vez dentro, configúralo de acuerdo a las siguientes indicaciones:

### Pasos para configurar tu Codespace:


1. Accede a la **Paleta de Comandos** presionando **F1** o haciendo clic en el menú ☰ y seleccionando **View** → **Command Palette**.

2. Comienza a escribir **dev container** en la Paleta de Comandos.

3. Selecciona **Codespaces: Add Development Container Configuration Files...**.

4. Selecciona **Create a new configuration...**.

5. Selecciona **From a predefined container configuration...**.

6. Desplázate hacia abajo y selecciona **Node.js & Mongo DB**.

7. Selecciona **20 (default)** para la versión de Node.js.

8. En la siguiente pantalla, selecciona **Azure CLI devcontainers** y **GitHub CLI devcontainers** de las características adicionales y luego selecciona **OK**.

    - **NOTA:** Puedes escribir el nombre de la característica que deseas para filtrar la lista.

9. Selecciona **Keep defaults**.

    - Esto creará los archivos de definición del nuevo contenedor en la carpeta `.devcontainer`.

10. Abre la **Paleta de Comandos** nuevamente.

11. Escribe **rebuild** y selecciona **Codespaces: Rebuild container**.

12. Selecciona **Rebuild Container** en el cuadro de diálogo. Ahora tu contenedor se reconstruirá.

    - **IMPORTANTE:** La reconstrucción del contenedor puede tardar varios minutos.


Una vez creado el Codespace y configurados los recursos, podrás ejecutar la aplicación con el siguiente comando:

```bash
npm run dev
```

## Criterios de Éxito

- Has creado y configurado un entorno de desarrollo en la nube con los siguientes recursos instalados:
  - GitHub CLI
  - Azure CLI
  - MongoDB
- Has creado un secreto encriptado para MONGODB_URI
- Eres capaz de iniciar y ver la aplicación en el entorno de desarrollo basado en la nube.
- Todos los cambios se fusionan en 'main'.
- **No** se instalaron recursos en tu máquina.

## Recursos de Aprendizaje

- [GitHub Codespaces](https://docs.github.com/es/codespaces/overview)
- [Introducción a los contenedores dev](https://docs.github.com/es/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers)
- [Configuración de un proyecto de Node.js para GitHub Codespaces](https://docs.github.com/es/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/setting-up-your-nodejs-project-for-codespaces)
- [Adición de características a un archivo devcontainer.json](https://docs.github.com/es/codespaces/setting-up-your-project-for-codespaces/configuring-dev-containers/adding-features-to-a-devcontainer-file)
- [Reenviar puertos en tu codespace](https://docs.github.com/es/codespaces/developing-in-a-codespace/forwarding-ports-in-your-codespace)
- [Administración de secretos específicos de la cuenta para GitHub Codespaces](https://docs.github.com/es/codespaces/managing-your-codespaces/managing-your-account-specific-secrets-for-github-codespaces)
- [Desarrollar en un codespace](https://docs.github.com/es/codespaces/developing-in-a-codespace/developing-in-a-codespace)
- [Precompilación de los codespaces](https://docs.github.com/es/codespaces/prebuilding-your-codespaces)

## Tips

- **Ctl-\`** mostrará la ventana de la terminal en Codespaces.
- **Cmd-Shift-P** (Mac) o **Ctl-Shift-P** (PC) abrirá la paleta de comandos.

[< Reto Anterior](./Challenge-00.md) - **[Home](../README.md)** - [Siguiente reto >](./Challenge-02.md)
