# Ерөнхий үйлдлүүд

- `SELECT` - Дата авах
- `INSERT INTO` - Шинийг авах
- `UPDATE  ... SET` - Өөрчлөлт оруулах
- `DELETE FROM` - Устгах

## Жишээ :

- `SELECT * FROM "BaStmt" WHERE 'StmtId' = 1`

  1. `Select` - Дата авах
  2. `*` - Бүх баганы датаг
  3. `FROM` - хаанаас
  4. `WHERE` - Ямар

  ### Өөрөөр хэлбэл BaStmt ээс StmtId нь 1 гэсэн бүх датаг авна гэж байна.

- `SELECT * FROM "CustCustomer" ca WHERE ca.'CustCode' = 1`

  1. `Select` - Дата авах
  2. `*` - Бүх баганы датаг
  3. `FROM "CustCustomer" ca ` - CustCustomer гэдэг table ээс дата авах ба тухайн авсан датанаас ямар нэгэн хувьсагч хэрэглэх бол `ca` гэж нэрлэнэ
  4. `WHERE` - Ямар
  5. `WHERE ca.'CustCode' = 1` - `ca` гэсэн хувьсагчид хадгалсан утгуудаас `CustCode` нь 1 тэй тэнцүүг авий

  ### Өөрөөр хэлбэл CustCustomer гэдэг table ийн утгыг ca гэдэг хувьсагчид оноож ca дотроос Custcode нь 1 тэйг тэнцүү утгыг авья

- `SELECT ca."CustCode" , cp."FirstName"  from main."CustCustomer" ca INNER JOIN main."CustPerson" cp  on ca."CustCode"  = cp."CustCode" where ca."CustCode" = '521000015'`
  1. `Select` - Дата авах
  2. `ca."CustCode" , cp."FirstName" ` - ca хувьсагч доторх CustCode гэсэн утгыг , cp дотор хадгалсан FirstName гэсэн утгыг авья
  3. `FROM "CustCustomer" ca ` - CustCustomer гэдэг table ээс дата авах ба тухайн авсан датанаас ямар нэгэн хувьсагч хэрэглэх бол `ca` гэж нэрлэнэ
  4. `INNER JOIN main."CustPerson" cp  on ca."CustCode"  = cp."CustCode"` - CustPerson гэсэн table ээс дата мөр бүр дээр нэгтгэнэ. Гэхдээ ca утга дээрх CustCode нь cp дээрх CustCode той тэнцүү байгаа нөхцөлд хамтад нь нэг мөрөнд гаргана
  5. `WHERE` - Ямар
  6. `WHERE ca.'CustCode' = 1` - `ca` гэсэн хувьсагчид хадгалсан утгуудаас `CustCode` нь 1 тэй тэнцүүг авий
  ### Өөрөөр хэлбэл CustCustomer гэдэг table ийн утгыг ca гэдэг хувьсагчид оноож ca дотроос Custcode нь 521000015 тэйг тэнцүү утгуудаас зөвхөн CustCode болон FirstName гэсэн утгуудыг авья
