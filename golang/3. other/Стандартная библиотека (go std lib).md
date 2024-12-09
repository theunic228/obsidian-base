Стандартная библиотека Go предоставляет мощный и разнообразный набор пакетов для выполнения задач практически любого уровня сложности. Она охватывает базовые аспекты программирования, такие как ввод/вывод, работа с сетью, обработка строк, управление процессами и многое другое.
### **1. Основные категории стандартной библиотеки Go**

#### **1.1. Базовые утилиты**

- **`fmt`**: Форматированный ввод/вывод.
```go
fmt.Println("Hello, World!")
fmt.Printf("Hello, %s!\n", "Gopher")
```
- **`errors`**: Создание и работа с ошибками.
```go
import "errors"
err := errors.New("something went wrong")
```
- **`strconv`**: Преобразование строк и чисел.
```go
import "strconv"
num, _ := strconv.Atoi("123") // Преобразование строки в число
str := strconv.Itoa(123)      // Преобразование числа в строку
```
#### **1.2. Работа с коллекциями**

- **`sort`**: Сортировка массивов и слайсов.
```go
import "sort"
numbers := []int{5, 2, 6, 3, 1}
sort.Ints(numbers)
fmt.Println(numbers) // [1 2 3 5 6]
```
- **`container/heap`**: Реализация куч (heap).
- **`container/list`**: Двусвязные списки.
#### **1.3. Работа с текстом**

- **`strings`**: Операции со строками.
```go
import "strings"
s := "Hello, World!"
fmt.Println(strings.ToUpper(s)) // HELLO, WORLD!
```
- **`regexp`**: Работа с регулярными выражениями.
```go
import "regexp"
matched, _ := regexp.MatchString(`^Hello`, "Hello, World!")
fmt.Println(matched) // true
```
#### **1.4. Работа с временем**

- **`time`**: Управление временем и датами.
```go
import "time"
now := time.Now()
fmt.Println(now.Format("2006-01-02 15:04:05"))
```
#### **1.5. Работа с файлами и процессами**

- **`os`**: Работа с операционной системой (файлы, переменные среды, процессы).
```go
import "os"
file, err := os.Create("example.txt")
if err != nil {
    fmt.Println("Error:", err)
}
defer file.Close()
```
- **`io` и `io/ioutil`**: Чтение/запись данных.
```go
import "io/ioutil"
data, _ := ioutil.ReadFile("example.txt")
fmt.Println(string(data))
```
#### **1.6. Работа с сетью**

- **`net`**: Низкоуровневые сетевые операции.
```go
import "net"
conn, _ := net.Dial("tcp", "golang.org:80")
conn.Write([]byte("GET / HTTP/1.0\r\n\r\n"))
```
- **`net/http`**: Создание HTTP-серверов и клиентов.
```go
import "net/http"
func handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintln(w, "Hello, World!")
}
http.HandleFunc("/", handler)
http.ListenAndServe(":8080", nil)
```
#### **1.7. Работа с кодированием и форматами данных**

- **`encoding/json`**: Работа с JSON.
```go
import "encoding/json"
type Person struct {
    Name string `json:"name"`
    Age  int    `json:"age"`
}
person := Person{"Alice", 30}
jsonData, _ := json.Marshal(person)
fmt.Println(string(jsonData)) // {"name":"Alice","age":30}
```
- **`encoding/xml`**: Работа с XML.
- **`encoding/csv`**: Работа с CSV.
#### **1.8. Конкурентность**

- **`sync`**: Синхронизация потоков.
```go
import "sync"
var mu sync.Mutex
mu.Lock()
// критическая секция
mu.Unlock()
```
- **`sync/atomic`**: Работа с атомарными операциями.
- **`context`**: Управление контекстом выполнения.
```go
import "context"
ctx, cancel := context.WithCancel(context.Background())
go func() {
    // Выполняется в отдельной горутине
    <-ctx.Done() // Ожидание завершения контекста
}()
cancel()
```
#### **1.9. Криптография**

- **`crypto`**: Базовые криптографические функции.
- **`crypto/md5` и `crypto/sha256`**: Хеширование.
```go
import (
    "crypto/sha256"
    "fmt"
)
data := []byte("hello world")
hash := sha256.Sum256(data)
fmt.Printf("%x\n", hash)
```
#### **1.10. Работа с тестированием**

- **`testing`**: Написание тестов.
```go
import "testing"
func TestSum(t *testing.T) {
    result := 2 + 2
    if result != 4 {
        t.Errorf("Expected 4, got %d", result)
    }
}
```

### **2. Полезные пакеты стандартной библиотеки**

|**Пакет**|**Описание**|
|---|---|
|**`flag`**|Работа с аргументами командной строки.|
|**`math`**|Базовые математические операции.|
|**`math/rand`**|Генерация случайных чисел.|
|**`path/filepath`**|Работа с путями файлов.|
|**`log`**|Логирование.|
|**`reflect`**|Работа с отражением (reflection).|
|**`unicode`**|Функции для работы с символами Unicode.|
|**`bufio`**|Буферизированный ввод/вывод.|

Стандартная библиотека Go устанавливается вместе с языком и находится в директории, указанной в переменной окружения `GOROOT`. Она является частью установленного дистрибутива Go и располагается в поддиректории `src` внутри пути `GOROOT`.
