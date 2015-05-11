# Цель 

Доделать гем.

Реализовать:

* вложенные ключи
* наследование окружений

```ruby
Configus.build :development do
  env :production do
    email do
      server 'some-server'
      port 1234
      login 'login'
      password 'pass'
    end
    
    key1 do
      key2 do
        key3 do
          key4 'value'
        end
      end
    end
  end

  # именованый параметр parent
  env :development, parent: :production do
    email do
      server 'test-server'
    end
  end
end

Configus.config.email.server #=> 'test-server'
Configus.config.email.port #=> port
Configus.config.email.to_h #=> { server: 'test-server', port: 1234, login: 'login', password: 'pass' }

Configus.config.key1.key2.key3.key4 #=> 'value'
Configus.config.key1.key2.key3.to_h #=> { key4: 'value' }
```

# Полезности

## Рекурсивное объединение хэшей

```ruby
# метод модифицирует target
def deep_merge(target, source)
  source.each do |k, v|
    tv = target[k]
    target[k] = tv.is_a?(Hash) && v.is_a?(Hash) ? deep_merge(tv, v) : v
  end
  target
end
```
