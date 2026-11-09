# SaraIA para Revit · descargas

Instaladores públicos de SaraIA, el asistente de IA para Autodesk Revit. Cada versión tiene su etiqueta y una [Release](../../releases) con el instalador adjunto.

**Última versión: [v1.2.1](../../releases/tag/v1.2.1)** · [Descargar el instalador](https://github.com/CMEDUCATIVA/saraia-revit-releases/releases/download/v1.2.1/SaraIA_Revit_v1.2.1_6042617_Setup.exe)

## Versiones

| Versión | Fecha | Revit | Instalador | SHA-256 |
|---|---|---|---|---|
| [1.2.1](../../releases/tag/v1.2.1) | 2026-11-09 | 2022 a 2027 | `SaraIA_Revit_v1.2.1_6042617_Setup.exe` | `ac0044ffe08ad6c2e7a87a7716731761e055d05ca9452d88b3246f9a5e9d1380` |
| [1.2.0](../../releases/tag/v1.2.0) | 2026-10-22 | 2022 a 2027 | `SaraIA_Revit_v1.2.0_b87a2be_Setup.exe` | `6b7146f3c349bc415375a4456fb5b9a8a37177f3574af31fc0b25f606d13371e` |

## Instalar

1. Guarda tu trabajo y cierra Revit.
2. Descarga el instalador de la última versión y, si quieres, comprueba su SHA-256 (en PowerShell: `Get-FileHash .\SaraIA_Revit_v1.2.1_6042617_Setup.exe`).
3. Ejecútalo y elige las versiones de Revit donde quieres SaraIA. Si detecta una instalación anterior, ofrece limpiarla.
4. Abre Revit: aparece la pestaña **SaraIA**.

## Control API: un puerto por versión de Revit

Desde la 1.2.1, cada versión de Revit tiene su propia Control API, con su puerto y su token, así que dos Revit abiertos a la vez responden los dos. En la 1.2.0 todas usaban el puerto 8757.

| Revit | Puerto | Configuración |
|---|---|---|
| 2022 | 8772 | `%AppData%\Bibim\control_api.2022.json` |
| 2023 | 8773 | `%AppData%\Bibim\control_api.2023.json` |
| 2024 | 8774 | `%AppData%\Bibim\control_api.2024.json` |
| 2025 | 8775 | `%AppData%\Bibim\control_api.2025.json` |
| 2026 | 8776 | `%AppData%\Bibim\control_api.2026.json` |
| 2027 | 8777 | `%AppData%\Bibim\control_api.2027.json` |

`%AppData%\Bibim\control_api.json` es el índice: arriba, el puerto y el token del último Revit abierto; en `instances`, cada versión con su `port`, `token`, `url` y `running`. El botón **Endpoints** de la pestaña SaraIA muestra la URL y el token de tu Revit.
