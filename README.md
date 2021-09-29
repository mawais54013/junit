# Junit For CI-Visibility

JUnit test report files are XML files that contain test execution information, such as test and suite names, pass/fail status, duration, and sometimes error logs. Although it was introduced by the JUnit testing framework, many other popular frameworks are able to output results using this format.

## Setup
Install datadog-ci cli globally using npm: <br/>
```
npm install -g @datadog/datadog-ci
```

## Execution 
Clone this repo down to desktop directory or any other path

Run this command below:
If on desktop directory:
```
DD_ENV=ci DATADOG_API_KEY=<API KEY HERE/> npx datadog-ci  junit upload \
  --service my-api-service \
  /Users/muhammad.awais/Desktop/junit/junit.xml
```

```
datadog-ci junit upload --service <service_name> <path> [<path> ...]
```

## Results:
Should be shown in datadog ci after a couple of minutes: https://app.datadoghq.com/ci/test-runs?index=citest&start=1632627253983&end=1632630853983&paused=false 

## Documentation
https://docs.datadoghq.com/continuous_integration/setup_tests/junit_upload/