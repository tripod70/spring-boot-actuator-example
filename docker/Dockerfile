FROM openjdk:8-jre-slim
RUN groupadd -r user && \
    useradd -r -g user -m -s /usr/bin/nologin -c "Docker image user" user
#COPY --chown=user:user --from=builder /app/target/app.jar /home/user
COPY ./target/*.jar /home/user/app.jar; done
USER user
WORKDIR /home/user
ENTRYPOINT ["java", "-jar", "app.jar", ]
