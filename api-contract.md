## Mahasiswa
<details>
<summary> Klik untuk Ekspan </summary>

### Create Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Rusdi Abdul Gani",
    "alamat" : "Ciawi",
    "hoby" : "Coding"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Mahasiswa berhasil diinput",
    "data" : {
        "id" : 2003,
        "nama" : "Rusdi Abdul Gani",
        "alamat" : "Ciawi",
        "hoby" : "Coding"
        
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Mahasiswa telah digunakan",
    "data" : {
        "value" : "Rusdi Abdul Gani",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Mahasiswa By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=2003 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=2003 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 2003,
        "nama" : "Rusdi Abdul Gani",
        "alamat" : "Ciawi",
        "hoby" : "Coding"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 2003,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Mahasiswa All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 2003,
            "nama" : "Rusdi Abdul Gani",
            "alamat" : "Ciawi",
            "hoby" : "Coding"
        },
        {
            "id" : 2004,
            "nama" : "Amir Lag",
            "alamat" : "Megamendung",
            "hoby" : "Musik"
        },
        {
            "id" : 2005,
            "nama" : "Ari Kriting",
            "alamat" : "Bogor",
            "hoby" : "Animasi"
        },
        {
            "id" : 2006,
            "nama" : "Fatur Lucas",
            "alamat" : "Bogor",
            "hoby" : "Ceramah"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 2003,
    "nama" : "Rusdi Abdul Gani",
    "alamat" : "Bogor",
    "hoby" : "Coding dan Desain"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Mahasiswa berhasil diubah",
    "data" : {
        "id" : 2003,
        "nama" : "Rusdi Abdul Gani",
        "alamat" : "Bogor",
        "hoby" : "Coding dan Desain"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Mahasiswa telah digunakan",
    "data" : {
        "value" : "Rusdi Abdul Gani",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 2003,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Mahasiswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=2003 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=2003 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [
        {
            "id" : 2003,
            "nama" : "Rusdi Abdul Gani",
            "alamat" : "Bogor",
            "hoby" : "Coding dan Desain"
        }
    ] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mahasiswa tidak ditemukan",
    "data" : {
        "value" : 2003,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

## Mata Kuliah
<details>
<summary> Klik untuk Ekspan </summary>

### Create Mata Kuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matkul </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "matkul" : "Pemrograman Berbasis Web",
    "dosen pengampu" : "MASHUM ABDUL JABBAR",
    "sks" : 3,
    "kelas" : "ILKOM 101"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Matkul berhasil diinput",
    "data" : {
        "kodemk" : 001,
        "matkul" : "Pemrograman Berbasis Web",
        "dosen pengampu" : "MASHUM ABDUL JABBAR",
        "sks" : 3,
        "kelas" : "ILKOM 101"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Matkul Telah digunakan",
    "data" : {
        "value" : "Pemrograman Berbasis Web",
        "property" : "matkul",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Mata Kuliah By kodemk
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matkul </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/matkul?kodemk=001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> kodemk=001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "kodemk" : 001,
        "matkul" : "Pemrograman Berbasis Web",
        "dosen pengampu" : "MASHUM ABDUL JABBAR",
        "sks" : 3,
        "kelas" : "ILKOM 101"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "Kodemk Matkul tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "kodemk",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Mata Kuliah All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matkul </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "kodemk" : 001,
            "matkul" : "Pemrograman Berbasis Web",
            "dosen pengampu" : "MASHUM ABDUL JABBAR",
            "sks" : 3,
            "kelas" : "ILKOM 101"
        },
        {
            "kodemk" : 002,
            "matkul" : "Basis Data 2",
            "dosen pengampu" : "UUS FIRDAUS",
            "sks" : 3,
            "kelas" : "ILKOM 101"
        },
        {
            "kodemk" : 003,
            "matkul" : "Jaringan Komputer",
            "dosen pengampu" : "AZHARUDIN",
            "sks" : 4,
            "kelas" : "ILKOM 101"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update Mata Kuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matkul </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "kodemk" : 001,
    "matkul" : "Pemrograman Berbasis Web",
    "dosen pengampu" : "MASHUM ABDUL JABBAR",
    "sks" : 4,
    "kelas" : "Smart Class"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Matkul Berhasil diubah",
    "data" : {
        "kodemk" : 001,
        "matkul" : "Pemrograman Berbasis Web",
        "dosen pengampu" : "MASHUM ABDUL JABBAR",
        "sks" : 4,
        "kelas" : "Smart Class"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Matkul Telah digunakan",
    "data" : {
        "value" : "Pemrograman Berbasis Web",
        "property" : "matkul",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "Kodemk Matkul tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "kodemk",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Mata Kuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matkul </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/matkul?kodemk=001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> kodemk=001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [
        {
            "kodemk" : 001,
            "matkul" : "Pemrograman Berbasis Web",
            "dosen pengampu" : "MASHUM ABDUL JABBAR",
            "sks" : 4,
            "kelas" : "Smart Class"
        }
    ] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "kodemk Matkul tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "kodemk",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>