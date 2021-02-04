db-first
<!-- Istruzioni:
Create un file di testo per descrivere un database di un negozio di videogiochi.
Strutturate il file come fatto oggi in classe.  Specificate: il nome del database, la tabella e le potenziali colonne con i tipi di dato. -->

# database name : Ludoteca
# nome tabella : Videogiochi

- id BIGINT PRIMARYKEY NOTNULL AUTO_INCREMENT
- isbn string VARCHAR(15) NOTNULL UNIQUE
- title string VARCHAR(255) NOTNULL
- description string TEXT NULL
- author string VARCHAR(30) NOTNULL
- year_release date YEAR NOTNULL
- genre string VARCHAR(15) NOTNULL
- price int FLOAT(5,2) NULL
- production_company string VARCHAR(50) NULL
- availability int TINYINT NULL DEFAULT(0)
- multyplatform int TINYINT NULL DEFAULT(0)
- platform string VARCHAR(100) NULL 
- cover_img string VARCHAR() NULL
- disk int TINYINT NULL
- version string VARCHAR(20) NULL <!-- disk or digital-->
- topic VARCHAR(30) NOTNULL
- language string VARCHAR() NOTNULL
- subtitles string VARCHAR() NULL
- edition string VARCHAR(30) NULL
- quantity int SMALLINT NULL DEFAULT(0)
- min_storage string VARCHAR (25) NULL
- players int TINYINT NULL
- pegi_info int TINYINT NULL
- created_at_date date DATETIME NOTNULL
- edited_in date DATETIME NULL