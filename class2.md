# CI (Continous Integration)

* When we push code there should be a pipeline that should automatically:
    * Download code --> Linting --> Building --> Unit Testing(mocking and testing) --> SCA(Software Compliance Analysis) --> SAST(Static Analysis Security Testing) --> Dockerize(create Images) --> Testing --> Push Image into Artifact repository  