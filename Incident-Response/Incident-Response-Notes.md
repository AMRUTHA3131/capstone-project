# Incident Response and Log Review

## Objective

The objective of this exercise is to practice a basic incident-response workflow using the local DVWA Docker environment. This is a simulated training activity, not a real production incident.

## Environment

- Application: DVWA
- Container: `dvwa-dvwa-1` 
- Environment: Local Docker lab
- Testing source: Local machine

## Log Collection

Check the running containers:

```
sudo docker ps
```

Review recent application container logs:

```
sudo docker logs --tail 50 dvwa-dvwa-1
```

Check whether an Apache access-log directory exists inside the container:

```
sudo docker exec dvwa-dvwa-1 sh -c 'ls -l /var/log/apache2/'
```

If an access log exists, inspect its recent entries:

```
sudo docker exec dvwa-dvwa-1 sh -c 'tail -n 50 /var/log/apache2/access.log'
```

## Evidence and Observations

- Application logs available: No
- Access log available: No

## Analysis

- Request path and HTTP method
- Timestamp
- HTTP status code
- Repeated or unusual requests
- Errors associated with the test
- Whether the event can be linked to the controlled test

A suspicious-looking request is not automatically proof of compromise. Correlate the request with the test activity and application response.

## Containment

For this lab, containment may involve stopping the test, restricting access to the local service, or stopping the DVWA containers if required.

Example command to stop the application stack from its Compose project directory:

```
sudo docker compose down
```

## Lessons Learned

- Record relevant evidence during testing.
- Preserve useful logs before changing the environment.
- Use multiple sources to investigate an event.
- Apply and verify remediation.
- Document limitations and unresolved questions.

## Conclusion

This exercise documents the process of reviewing available logs and recording a controlled security test. The findings are limited to the evidence actually collected from the local lab.
