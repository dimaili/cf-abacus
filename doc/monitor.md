Monitoring Abacus applications using Hystrix Dashboard
===

Building Hystrix Dashboard
---

Get latest customized Hystrix Dashboard

```bash
git clone https://github.com/sasrin/Hystrix
cd Hystrix
git checkout dev
git pull
```

Build the dashboard using Gradle

```bash
cd hystrix-dashboard
../gradlew build
```

The build creates Hystrix Dashboard web application at ./build/libs/hystrix-dashboard-X.X.X-SNAPSHOT.war

Run the dashboard using Jetty

```bash
../gradlew jettyRun
```

Monitoring with Hystrix
---

Access the dashboard at `http://localhost:7979/hystrix-dashboard`

Add hystrix streams from Abacus applications:
* Enter hystrix steam URL for an application. For example, the usage collector application running at local machine would have hystrix stream reachable at `http://localhost:9080/hystrix.stream`
* Enter a title for an application
* Uncheck *Monitor Thread Pools*
* Click *Add Stream*
* Repeat the above steps for each application

Click *Monitor Streams* to monitor the applications