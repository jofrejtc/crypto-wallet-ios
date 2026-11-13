# Crypto Wallet iOS

Aplicación académica en Swift y UIKit para consultar precios y seguir una cartera. Utiliza Firebase Authentication para las sesiones, Alamofire para consultar CoinRanking y Core Data para la persistencia local.

## Aportación de Jofre

Implementé los modelos `Decodable` de `CryptoAPIModels.swift`, que convierten las respuestas JSON de CoinRanking en los datos que usa la aplicación.

## Ejecutar en local

Descarga [el proyecto completo](crypto-wallet-ios.zip), descomprime el ZIP y abre la carpeta `crypto-wallet-ios` antes de seguir los pasos de esta sección.

1. Abre el archivo `.xcodeproj` de `src/` en Xcode 16.2 o posterior. El proyecto tiene como destino iOS 18.2.
2. Configura un proyecto de Firebase propio, activa Authentication por correo y contraseña, y añade tu `GoogleService-Info.plist` al target de la app. Registra el identificador de bundle que uses en Xcode.
3. Para consultar precios desde el simulador, añade `RAPIDAPI_KEY` en **Product → Scheme → Edit Scheme → Run → Arguments → Environment Variables**. Usa un esquema local sin compartir y tu propia clave de RapidAPI con acceso a CoinRanking.
4. Ejecuta la app desde Xcode. Si falta la variable, la app omite la consulta de mercado.

El repositorio está pensado para una demostración local. Si se distribuye la app, las llamadas a CoinRanking deben pasar por un servidor que custodie la clave.

## Verificación

Se verificaron la sintaxis de Swift, los archivos de proyecto de Xcode y la resolución de dependencias. La compilación completa y la ejecución en simulador siguen pendientes.

## Equipo y licencia

Trabajo académico de Eric Faya, Guillem Gil y Jofre Tura Centelles. Guillem publicó el repositorio original. Esta copia conserva la licencia MIT y su aviso de copyright en `LICENSE`.
