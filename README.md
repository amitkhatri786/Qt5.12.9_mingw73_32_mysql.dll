# Qt5.12.9_mingw73_32_mysql.dll
Mysql driver for QT5.12.9

 Compile with mingw73_32 bit for Qt5.12.9

mysql.pro changes
#QMAKE_USE += mysql

OTHER_FILES += mysql.json

PLUGIN_CLASS_NAME = QMYSQLDriverPlugin
include(../qsqldriverbase.pri)

LIBS += -L'C:\Users\Amit\Downloads\mysql-connector-c-6.1.11-win32\lib' -llibmysql
INCLUDEPATH += 'C:\Users\Amit\Downloads\mysql-connector-c-6.1.11-win32\include'
DEPENDPATH += 'C:\Users\Amit\Downloads\mysql-connector-c-6.1.11-win32\include'

Commands:

cd F:\QT5\qt-everywhere-src-5.12.9\qtbase\src\plugins\sqldrivers
qmake sqldrivers.pro
cd mysql
qmake mysql.pro
mingw32-make

Plugin location --> F:\QT5\qt-everywhere-src-5.12.9\qtbase\src\plugins\sqldrivers\plugins\sqldrivers
Put .dll inside installation directory of qt--> F:\Qt\Qt5.12.9\5.12.9\mingw73_32\plugins\sqldrivers
put libmysql.dll inside build binary folder--> F:\Qt\Qt5.12.9\5.12.9\mingw73_32\bin

Now run the program.
