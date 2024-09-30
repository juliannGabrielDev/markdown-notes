# Historia del Control de Versiones

Creado: 26 de septiembre de 2024 1:30

---

Como ya sabrá a estas alturas, el **control de versiones** es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo para poder acceder a versiones específicas más adelante. En el desarrollo de software, **los sistemas de control de versiones (VCS** ) permiten a los desarrolladores gestionar los cambios en su código y realizar un seguimiento de quién realizó cada cambio. Pero, ¿cómo surgió este software?

El control de versiones tiene una larga historia que se remonta a la década de 1980. De hecho, ¡los sistemas de control de versiones se crearon antes que Internet!

# Sistema de Versiones Concurrentes (CVS)

Uno de los primeros sistemas de control de versiones importantes fue el **Sistema de Versiones Concurrentes (CVS)**. Fue desarrollado por primera vez en 1986 por Walter F. Tichy en la Universidad de Purdue y lanzado públicamente en 1990.

El**CVS** almacena información sobre cada archivo en una estructura de carpetas, incluyendo el nombre del archivo, su ubicación en la estructura de carpetas, quién lo modificó por última vez y cuándo se modificó por última vez. El **CVS** también almacena información sobre las carpetas, incluyendo sus nombres y quién las creó.

Fue popular durante muchos años; sin embargo, tiene algunos defectos importantes en su diseño. El **CVS** no incluye comprobaciones de integridad, lo que significa que sus datos pueden corromperse. Cuando usted actualiza o envía cambios al sistema, si se produce un error, el sistema acepta los archivos parciales o corruptos. Además, el sistema se diseñó principalmente para archivos de texto, no para archivos binarios como imágenes o vídeos.

# Subversion (SVN)

El principal sucesor de **CVS** fue **Subversion (SVN)**.

CollabNet desarrolló Subversion en 2000 y resolvió muchos de los problemas presentes en **CVS**. Para garantizar la integridad de los datos, incluyó comprobaciones de integridad en su diseño. También soportaba el versionado de archivos binarios mejor que **CVS**. Gracias a estas mejoras, SVN se hizo popular en la comunidad de código abierto y Google y SourceForge ofrecieron alojamiento gratuito para proyectos de código abierto.

Sin embargo, Subversion utilizaba un modelo **VCS** centralizado. Esto significa que todas las operaciones deben realizarse en un servidor centralizado. Si el servidor se caía o era lento, esto impediría el desarrollo.

En 2005, se iniciaron dos nuevos proyectos para desarrollar sistemas de control de versiones distribuidos: Mercurial y Git. Ambos proyectos se crearon en respuesta a un suceso relacionado con el desarrollo del núcleo de Linux.

Anteriormente, el núcleo Linux utilizaba un **VCS** propietario conocido como BitKeeper. BitKeeper fue uno de los primeros sistemas de control de versiones distribuidos, lanzado inicialmente en el año 2000. BitKeeper había proporcionado originalmente una licencia gratuita a Linus Torvalds para apoyar el desarrollo de Linux. Sin embargo, en 2005, la licencia fue revocada. Esta controversia llevó a la creación de los proyectos Mercurial y Git.

# Mercurial y Git

Mercurial fue desarrollado por Olivia Mackall. Se ha desarrollado como un **VCS** distribuido de alto rendimiento. Muchas plataformas que ofrecían alojamiento Subversion empezaron a ofrecer también alojamiento Mercurial. Se hizo popular porque los usuarios de Subversion encontraron fácil la transición a un repositorio Mercurial, gracias a los proveedores de alojamiento y a su pequeña curva de aprendizaje.

Git fue desarrollado por Linus Torvalds para alojar el código fuente del núcleo Linux. Al igual que Mercurial, es un **VCS** distribuido. Su primera versión pública se publicó en 2007.

Git se hizo popular en la comunidad de código abierto debido a su diseño de **VCS** distribuido y a que Github ofrecía alojamiento gratuito de Git para proyectos de código abierto. Desde entonces, Git se ha convertido en el sistema de control de versiones seleccionado para muchos proyectos de software de código abierto y propietario.