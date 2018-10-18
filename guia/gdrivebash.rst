Como configurar y ejecutar gdrive en bash
=======================================

Descargar el Google Drive CLI Client desde aquí:

https://github.com/prasmussen/gdrive

Lo ejecuta y debe seguir los pasos::

	$ gdrive-linux-x64 list
	Authentication needed
	Go to the following url in your browser:
	https://accounts.google.com/o/oauth2/auth?access_type=offline&client_id=367116221053-7n0vf5akeru7on6o2fjinrecpdoe99eg.apps.googleusercontent.com&redirect_uri=urn%3Aietf%3Awg%3Aoauth%3A2.0%3Aoob&response_type=code&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fdrive&state=state

	Enter verification code: 4/fAAQ5ueNFh4BGuM5I0s9vGk_jz5s6OXd_pAYMEB6OGsOwvg2f_hdaR0

	Id                                  Name                                 Type   Size       Created
	16M4ay5kkO2nkCeWTlM88v8Po2D_-KLbh   CONSIS-G-15784.ear                   bin    391.1 MB   2018-10-15 14:32:12
	1zyWwk1o8_UD2EgJp63O8GgEx_cibjfcV   G-6744                               dir               2018-10-15 10:07:56
	1-CVTu18Y4mmfkchuk83We0dLvDxfUSQZ   CONSIS.G-6744.ear                    bin    380.8 MB   2018-10-15 10:42:01
	1qJpOzrOTANCkyV4APb5KPMAP9BuDZrI6   generate-schematools-G-6744.tar      bin    68.5 MB    2018-10-15 10:23:43
	13hc6F_sE04OiHVQaOlZOBYji6lP8hogA   G-5710                               dir               2018-10-08 14:52:03
	1chRMpXL9S6tCURvaA1jBJJ-Ua4tk-R1p   generate-schematools-G-5710.tar.gz   bin    63.1 MB    2018-10-08 15:06:56
	1LBCiSyaUQLmfmHKw9GtfGhK7XS09s5wZ   Autodeploy_Rev-G-5710.tar.gz         bin    456.7 MB   2018-10-08 15:05:34
	1MyO1R-Llk2Cjz7l-zHl2AISSqyDngRH8   G-5709                               dir               2018-10-08 11:51:37
	1sYYMDZoQGgTkHdc5W__8iONj8kku3UxB   generate-schematools-G-5709.tar      bin    71.3 MB    2018-10-08 12:04:47


Subimos un archivo::

	$ gdrive-linux-x64 upload EAR-schematool.tar.gz
	Uploading EAR-schematool.tar.gz
	Uploaded 1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ at 1.1 MB/s, total 441.7 MB

Lo debemos compartir::

	$ gdrive-linux-x64 share 1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ
	Granted reader permission to anyone

Consultamos el archivo que subimos:

	gdrive-linux-x64 info 1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ
	Id: 1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ
	Name: EAR-schematool.tar.gz
	Path: EAR-schematool.tar.gz
	Mime: application/x-gzip
	Size: 441.7 MB
	Created: 2018-10-18 12:58:10
	Modified: 2018-10-18 12:58:10
	Md5sum: d39aebdaca81e1e792eecb7af92940db
	Shared: False
	Parents: 0ABUfMcsjOXfxUk9PVA
	ViewUrl: https://drive.google.com/file/d/1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ/view?usp=drivesdk
	DownloadUrl: https://drive.google.com/uc?id=1p47OzaHRvdZ5qyD0M3vewF6RJqf5fqXQ&export=download




