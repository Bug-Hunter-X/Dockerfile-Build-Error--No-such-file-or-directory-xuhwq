This repository contains a Dockerfile with a common error and its solution. The original Dockerfile fails to build because it tries to copy and install dependencies from a missing requirements.txt file.  The solution demonstrates how to properly handle dependencies and build a Docker image.

**Error:**

The Docker build process will fail with an error similar to: `ERROR: Service 'web' failed to build: COPY failed: stat /var/lib/docker/tmp/docker-builderXXX/requirements.txt: no such file or directory`

**Solution:**

The solution involves ensuring that the requirements.txt file exists in the build context and that the path in the Dockerfile is correct.