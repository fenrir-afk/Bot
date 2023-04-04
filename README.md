# Bot
ChatBot
  Это телеграм бот,умеющий выводить расписание преподователей,карту, а также отправлять рассылки важной информации.
Для создания данного бота нам понадобися:
dependencies {
    flywayMigration("org.postgresql:postgresql:$postgresVersion")
    jooqGenerator("org.postgresql:postgresql:$postgresVersion")
    runtimeOnly("org.postgresql:postgresql")

   //Классические стартеры spring boot
    implementation("org.springframework.boot:spring-boot-starter")
    implementation("org.springframework.boot:spring-boot-starter-jooq")
    implementation("org.springframework.boot:spring-boot-starter-freemarker")
    implementation("org.springframework.boot:spring-boot-starter-web")

    implementation("org.telegram:telegrambots:$telegramBotVersion")
    implementation("org.telegram:telegrambotsextensions:$telegramBotVersion")
    implementation("org.telegram:telegrambots-spring-boot-starter:$telegramBotVersion")

    // зависимости, которые помогут сгенерить метаданные
    compileOnly("org.springframework.boot:spring-boot-configuration-processor")
    annotationProcessor("org.springframework.boot:spring-boot-configuration-processor")
    testImplementation("org.springframework.boot:spring-boot-starter-test")
}
 Обоснования выбора технологий:

  Spring Boot и весь Spring Framework в JVM мире стал неотъемлемой частью создания больших и сложных энтерпрайз систем.
Пал выбор именно на него, так как порой хочется сделать не просто бота,
а полноценное приложение, которым будет удобно пользоваться и удобно масштабировать.
  JOOQ — механизм, который помогает на DSL подобном языке формировать sql запросы.
  Freemarker — шаблонизатор, необходим для формирования динамичных текстовок
  PostgreSQL — СУБД. Тут субъективный выбор. Считаю его лучшим из бесплатных инструментов.
  org.telegram.telegrambots — набор библиотек для Telegram Api
  Чтобы запустить:
следует прописать команду /start
