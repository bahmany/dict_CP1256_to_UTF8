# dict_CP1256_to_UTF8
when we want to retrieve data in json via pymssql, and database collation is  SQL_Latin1_General_CP1256_CI_AS we should convert all str to utf8

when you have connection like this :

            conn = pymssql.connect(server=connectionInstance.hostAddress,
                                   user=connectionInstance.username,
                                   password=connectionInstance.password,
                                   database=connectionInstance.databaseName,
                                   # charset="UTF-8",
                                   as_dict=True)
            cursor = conn.cursor(as_dict=True)
            cursor.execute(sql)
            result = cursor.fetchall()
            result = convert_sqlresultstr_to_valid_str(result)





