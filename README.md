# Escrevendo-no-Celular
### Repositório para criar os casos de teste da questão do DojoPuzzles "Escrevendo no Celular" 
  * Membros: Alan David, Lucas de Lima
  * Problema: [link](http://dojopuzzles.com/problemas/exibe/escrevendo-no-celular/)
  * Tecnologia: Php com Laravel 5.4
  
  
  ## Plano de teste

| Entrada  | Condição | Classes Válidas | Classes Inválidas |
| ------------- | ------------- | ------------- | ------------- |
| Cadeia de Caracteres      |Cadeia Igual ah string  | is_string($cadeia) == True | is_string($cadeia) != True |
| Cadeia de Caracteres      |Cadeia Menor ou Igual ah 255 Caracteres | strlen ( string $cadeia ) <= 255 | strlen ( string $cadeia ) > 255 |
| Cadeia de Caracteres      |Cadeia ser diferente de vazia  | strlen > 0 | strlen <= 0  |

 ### Protótipos dos métodos

```php
asciiToGSM(String $cadeia)
```

### 1º Caso de Teste

```php
asciiToGSM("a") // Retorna a Cadeia de numeros "1"
```

### 2º Caso de Teste

```php
asciiToGSM(1) // Retorna UnexpectedValueException
```

### 3º Caso de Teste

```php
asciiToGSM("Gol de mao") // Retorna a Cadeia de numeros "46665550333062666"
```

### 4º Caso de Teste

```php
asciiToGSM("") // Retorna UnexpectedValueException
```

