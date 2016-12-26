# LuckyArchiver #

**Repositório do Projeto Archiver**

O objetivo do projeto é criar um conjunto de scripts capazes de indexar, organizar e manter arquivos no sistema de arquivos, bem como criar e manter backups.

------

## Resumo das idéias e comandos: ##

### Apagar arquivos duplicados do sistema de arquivos ###

Com esta opção é possível eliminar os arquivos duplicados, liberando espaço em disco, para isso é fornecida uma referência. Os arquivos do diretório analisado que estiverem na referência serão eliminados.

```
larch checkclones <dir_base>
	--reference <MEDIA:{ALL|HD|FLOPPY|OPTICAL|SDCARD|VIRTUAL}|dir_referencia>
	--recursive
	--no-name-match
	--forceupdate

	>> aclones.idx | eclones.idx & rclones.idx & oclones.idx
```

```
larch showclones <dir>
	--all
	--base
	--reference
	--unreference
	--expunge
```

```
larch addrule <dir>
	--reference <dir>
	--expunge <dir>
```

```
larch rmclones <dir>
	--makelinks
	--makesymbolic
```



