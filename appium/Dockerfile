FROM registry.access.redhat.com/ubi9/nodejs-18:1-112

USER root
RUN dnf install -y python3-pip
RUN chown -R appium:appium /app
USER appium

WORKDIR app

COPY ./requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
RUN npm i -g appium

RUN appium driver install uiautomator2
RUN appium driver install xcuitest
RUN appium driver install espresso


EXPOSE 4723

ENTRYPOINT ["appium"]