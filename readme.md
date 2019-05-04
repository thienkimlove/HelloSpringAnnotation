## Vi du co ban

`https://o7planning.org/vi/10127/huong-dan-lap-trinh-spring-cho-nguoi-moi-bat-dau`

### Nghien cuu vi du


* `@Component` là một annotation, nó được chú thích trên một class 

để nói với Spring rằng class này là một Spring BEAN. 
  
* `@Autowired` được chú thích trên một trường (field) 

để nói với Spring rằng hãy tiêm (inject) giá trị vào cho trường đó. 

Chú ý: Từ tiêm ở đây có ý giống với gán giá trị cho trường đó.

* `@Configuration` là một annotation, 

nó được chú thích trên một class, 

class này sẽ định nghĩa các Spring BEAN. 

* `@ComponentScan` 

- Nói cho Spring các package để tìm kiếm các Spring BEAN khác, 

Spring sẽ quét (scan) các package đó để tìm kiếm.

Các Spring BEAN được tạo ra sẽ được quản lý trong Spring IoC Container (Bộ chứa Spring `IoC`).

### How to run

* Bạn tạo một đối tượng ApplicationContext 


bằng cách đọc các cấu hình trong class AppConfiguration, 


giống như đoạn code dưới đây.

`ApplicationContext context = new AnnotationConfigApplicationContext(AppConfiguration.class);`

* Spring sẽ tạo các Spring BEAN, theo các định nghĩa trong class `AppConfiguration`, 


(Chú ý: Class AppConfiguration phải được chú thích bởi `@Configuration`).

* Tiếp theo Spring sẽ tìm kiếm trong package `"org.o7planning.spring.bean"`
 
 để tạo các Spring BEAN khác, 
 
 (Tạo các đối tượng từ các class được chú thích bởi `@Service`, `@Component` hoặc `@Repository`).
 
 * Lúc này các Spring BEAN đã được tạo ra, và được chứa trong Spring IoC.
  
  Các trường của các Spring BEAN có chú thích bởi @Autowired sẽ được tiêm các giá trị vào
  
  `https://o7planning.org/vi/10127/cache/images/i/4654923.png`