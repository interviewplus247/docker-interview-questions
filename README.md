# Docker Interview Questions & Answers

> A curated list of Docker interview questions covering Fundamentals, Architecture & Internals, Installation & Setup, Images, Containers, Dockerfiles, Networking, Volumes & Storage, Docker Compose, Registry & Docker Hub, Security, Docker Swarm & Orchestration, and Advanced & Scenario-Based Questions — each with a clear explanation and code example where applicable.

---

### Table of Contents

<details open>
<summary>
Hide/Show table of contents
</summary>

| No. | Questions |
| --- | --------- |
|     | **Docker Fundamentals** |
| 1 | [What is Docker and why was it created?](#what-is-docker-and-why-was-it-created) |
| 2 | [What problems does Docker solve?](#what-problems-does-docker-solve) |
| 3 | [What is containerization?](#what-is-containerization) |
| 4 | [How is Docker different from virtualization?](#how-is-docker-different-from-virtualization) |
| 5 | [What are the main components of Docker architecture?](#what-are-the-main-components-of-docker-architecture) |
| 6 | [What is the difference between Docker Engine and Docker Desktop?](#what-is-the-difference-between-docker-engine-and-docker-desktop) |
| 7 | [What is a Docker image?](#what-is-a-docker-image) |
| 8 | [What is a Docker container?](#what-is-a-docker-container) |
| 9 | [What is Docker Hub?](#what-is-docker-hub) |
| 10 | [What is the difference between an image and a container?](#what-is-the-difference-between-an-image-and-a-container) |
| 11 | [What happens internally when you run a Docker container?](#what-happens-internally-when-you-run-a-docker-container) |
| 12 | [What is the role of the Docker daemon?](#what-is-the-role-of-the-docker-daemon) |
| 13 | [What is the Docker CLI?](#what-is-the-docker-cli) |
| 14 | [What are the advantages of using Docker?](#what-are-the-advantages-of-using-docker) |
| 15 | [What are the limitations of Docker?](#what-are-the-limitations-of-docker) |
| 16 | [How does Docker achieve platform independence?](#how-does-docker-achieve-platform-independence) |
| 17 | [What is the difference between Docker CE and Docker EE?](#what-is-the-difference-between-docker-ce-and-docker-ee) |
| 18 | [What is the lifecycle of a Docker container?](#what-is-the-lifecycle-of-a-docker-container) |
| 19 | [What are common use cases of Docker?](#what-are-common-use-cases-of-docker) |
| 20 | [What are the prerequisites for running Docker?](#what-are-the-prerequisites-for-running-docker) |
|     | **Docker Architecture & Internals** |
| 21 | [Explain Docker architecture in detail](#explain-docker-architecture-in-detail) |
| 22 | [What is the role of dockerd?](#what-is-the-role-of-dockerd) |
| 23 | [What is containerd?](#what-is-containerd) |
| 24 | [What is runc?](#what-is-runc) |
| 25 | [How does Docker communicate with the Docker daemon?](#how-does-docker-communicate-with-the-docker-daemon) |
| 26 | [What is the Docker REST API?](#what-is-the-docker-rest-api) |
| 27 | [What is the purpose of Docker's client-server architecture?](#what-is-the-purpose-of-dockers-client-server-architecture) |
| 28 | [How does Docker interact with the Linux kernel?](#how-does-docker-interact-with-the-linux-kernel) |
| 29 | [What is a Docker registry?](#what-is-a-docker-registry) |
| 30 | [What is the difference between local and remote registries?](#what-is-the-difference-between-local-and-remote-registries) |
| 31 | [What are Docker namespaces?](#what-are-docker-namespaces) |
| 32 | [What are Linux cgroups?](#what-are-linux-cgroups) |
| 33 | [How do namespaces and cgroups work together?](#how-do-namespaces-and-cgroups-work-together) |
| 34 | [How does Docker isolate containers?](#how-does-docker-isolate-containers) |
| 35 | [What happens when the Docker daemon crashes?](#what-happens-when-the-docker-daemon-crashes) |
|     | **Installation & Setup** |
| 36 | [How do you install Docker on Linux?](#how-do-you-install-docker-on-linux) |
| 37 | [How do you install Docker on Windows?](#how-do-you-install-docker-on-windows) |
| 38 | [How do you install Docker on macOS?](#how-do-you-install-docker-on-macos) |
| 39 | [How do you verify a Docker installation?](#how-do-you-verify-a-docker-installation) |
| 40 | [What is the purpose of the hello-world image?](#what-is-the-purpose-of-the-hello-world-image) |
| 41 | [How do you configure Docker daemon settings?](#how-do-you-configure-docker-daemon-settings) |
| 42 | [How do you change Docker's default storage location?](#how-do-you-change-dockers-default-storage-location) |
| 43 | [How do you upgrade Docker?](#how-do-you-upgrade-docker) |
| 44 | [How do you uninstall Docker safely?](#how-do-you-uninstall-docker-safely) |
| 45 | [How do you troubleshoot Docker startup issues?](#how-do-you-troubleshoot-docker-startup-issues) |
|     | **Docker Images** |
| 46 | [What is a Docker image layer?](#what-is-a-docker-image-layer) |
| 47 | [How are Docker images built?](#how-are-docker-images-built) |
| 48 | [What is the union filesystem in Docker?](#what-is-the-union-filesystem-in-docker) |
| 49 | [What is image immutability?](#what-is-image-immutability) |
| 50 | [How do you list Docker images?](#how-do-you-list-docker-images) |
| 51 | [How do you inspect a Docker image?](#how-do-you-inspect-a-docker-image) |
| 52 | [How do you remove Docker images?](#how-do-you-remove-docker-images) |
| 53 | [What is the difference between image ID and digest?](#what-is-the-difference-between-image-id-and-digest) |
| 54 | [What are dangling images?](#what-are-dangling-images) |
| 55 | [How do you remove unused images?](#how-do-you-remove-unused-images) |
| 56 | [What is the difference between repository and tag?](#what-is-the-difference-between-repository-and-tag) |
| 57 | [What are image tags?](#what-are-image-tags) |
| 58 | [Why should images be versioned?](#why-should-images-be-versioned) |
| 59 | [What is the latest tag and why should it be avoided?](#what-is-the-latest-tag-and-why-should-it-be-avoided) |
| 60 | [What are base images?](#what-are-base-images) |
| 61 | [What are parent images?](#what-are-parent-images) |
| 62 | [What is a scratch image?](#what-is-a-scratch-image) |
| 63 | [What is the difference between Alpine and Ubuntu images?](#what-is-the-difference-between-alpine-and-ubuntu-images) |
| 64 | [How do image layers affect storage usage?](#how-do-image-layers-affect-storage-usage) |
| 65 | [How can image size be reduced?](#how-can-image-size-be-reduced) |
| 66 | [How do you view image history?](#how-do-you-view-image-history) |
| 67 | [What is image caching?](#what-is-image-caching) |
| 68 | [How do you export and import images?](#how-do-you-export-and-import-images) |
| 69 | [What is image digest verification?](#what-is-image-digest-verification) |
| 70 | [How do you scan Docker images for vulnerabilities?](#how-do-you-scan-docker-images-for-vulnerabilities) |
|     | **Containers Management** |
| 71 | [How do you create a Docker container?](#how-do-you-create-a-docker-container) |
| 72 | [What is the difference between docker create and docker run?](#what-is-the-difference-between-docker-create-and-docker-run) |
| 73 | [How do you start a stopped container?](#how-do-you-start-a-stopped-container) |
| 74 | [How do you stop a running container?](#how-do-you-stop-a-running-container) |
| 75 | [What is the difference between docker stop and docker kill?](#what-is-the-difference-between-docker-stop-and-docker-kill) |
| 76 | [How do you restart containers?](#how-do-you-restart-containers) |
| 77 | [How do you pause and unpause containers?](#how-do-you-pause-and-unpause-containers) |
| 78 | [What is container state management?](#what-is-container-state-management) |
| 79 | [How do you inspect a running container?](#how-do-you-inspect-a-running-container) |
| 80 | [How do you view container logs?](#how-do-you-view-container-logs) |
| 81 | [How do you execute commands inside a running container?](#how-do-you-execute-commands-inside-a-running-container) |
| 82 | [What is the difference between docker attach and docker exec?](#what-is-the-difference-between-docker-attach-and-docker-exec) |
| 83 | [How do you copy files into a container?](#how-do-you-copy-files-into-a-container) |
| 84 | [How do you copy files from a container?](#how-do-you-copy-files-from-a-container) |
| 85 | [How do you rename a container?](#how-do-you-rename-a-container) |
| 86 | [How do you remove containers?](#how-do-you-remove-containers) |
| 87 | [What are exited containers?](#what-are-exited-containers) |
| 88 | [How do you clean up unused containers?](#how-do-you-clean-up-unused-containers) |
| 89 | [What happens to data when a container is deleted?](#what-happens-to-data-when-a-container-is-deleted) |
| 90 | [How do you monitor container resource usage?](#how-do-you-monitor-container-resource-usage) |
| 91 | [How do you retrieve container metadata?](#how-do-you-retrieve-container-metadata) |
| 92 | [How do you limit CPU usage for containers?](#how-do-you-limit-cpu-usage-for-containers) |
| 93 | [How do you limit memory usage for containers?](#how-do-you-limit-memory-usage-for-containers) |
| 94 | [How do you limit disk I/O for containers?](#how-do-you-limit-disk-io-for-containers) |
| 95 | [How do you troubleshoot crashing containers?](#how-do-you-troubleshoot-crashing-containers) |
|     | **Dockerfile Instructions** |
| 96 | [What is a Dockerfile?](#what-is-a-dockerfile) |
| 97 | [How does a Dockerfile work?](#how-does-a-dockerfile-work) |
| 98 | [What are Dockerfile instructions?](#what-are-dockerfile-instructions) |
| 99 | [What is the FROM instruction?](#what-is-the-from-instruction) |
| 100 | [What is the RUN instruction?](#what-is-the-run-instruction) |
| 101 | [What is the CMD instruction?](#what-is-the-cmd-instruction) |
| 102 | [What is the ENTRYPOINT instruction?](#what-is-the-entrypoint-instruction) |
| 103 | [What is the difference between CMD and ENTRYPOINT?](#what-is-the-difference-between-cmd-and-entrypoint) |
| 104 | [What is the COPY instruction?](#what-is-the-copy-instruction) |
| 105 | [What is the ADD instruction?](#what-is-the-add-instruction) |
| 106 | [What is the difference between ADD and COPY?](#what-is-the-difference-between-add-and-copy) |
| 107 | [What is the WORKDIR instruction?](#what-is-the-workdir-instruction) |
| 108 | [What is the ENV instruction?](#what-is-the-env-instruction) |
| 109 | [What is the ARG instruction?](#what-is-the-arg-instruction) |
| 110 | [What is the difference between ENV and ARG?](#what-is-the-difference-between-env-and-arg) |
| 111 | [What is the EXPOSE instruction?](#what-is-the-expose-instruction) |
| 112 | [What is the USER instruction?](#what-is-the-user-instruction) |
| 113 | [What is the LABEL instruction?](#what-is-the-label-instruction) |
| 114 | [What is the VOLUME instruction?](#what-is-the-volume-instruction) |
| 115 | [What is the HEALTHCHECK instruction?](#what-is-the-healthcheck-instruction) |
| 116 | [What is the ONBUILD instruction?](#what-is-the-onbuild-instruction) |
| 117 | [How does the Docker build context work?](#how-does-the-docker-build-context-work) |
| 118 | [What is .dockerignore?](#what-is-dockerignore) |
| 119 | [How do you optimize Dockerfiles?](#how-do-you-optimize-dockerfiles) |
| 120 | [What are Dockerfile best practices?](#what-are-dockerfile-best-practices) |
| 121 | [What is a multi-stage Docker build?](#what-is-a-multi-stage-docker-build) |
| 122 | [Why are multi-stage builds important?](#why-are-multi-stage-builds-important) |
| 123 | [How do build arguments work?](#how-do-build-arguments-work) |
| 124 | [How can Docker build time be reduced?](#how-can-docker-build-time-be-reduced) |
| 125 | [How do you debug Dockerfile issues?](#how-do-you-debug-dockerfile-issues) |
|     | **Docker Networking** |
| 126 | [How does Docker networking work?](#how-does-docker-networking-work) |
| 127 | [What is the default bridge network?](#what-is-the-default-bridge-network) |
| 128 | [What is a bridge network?](#what-is-a-bridge-network) |
| 129 | [What is a host network?](#what-is-a-host-network) |
| 130 | [What is a none network?](#what-is-a-none-network) |
| 131 | [What is an overlay network?](#what-is-an-overlay-network) |
| 132 | [What is a macvlan network?](#what-is-a-macvlan-network) |
| 133 | [How do containers communicate with each other?](#how-do-containers-communicate-with-each-other) |
| 134 | [How does DNS resolution work in Docker?](#how-does-dns-resolution-work-in-docker) |
| 135 | [What is port mapping?](#what-is-port-mapping) |
| 136 | [What is the difference between EXPOSE and port publishing?](#what-is-the-difference-between-expose-and-port-publishing) |
| 137 | [How do you publish container ports?](#how-do-you-publish-container-ports) |
| 138 | [What is network isolation?](#what-is-network-isolation) |
| 139 | [How do you inspect Docker networks?](#how-do-you-inspect-docker-networks) |
| 140 | [How do you create custom networks?](#how-do-you-create-custom-networks) |
| 141 | [Why should custom networks be preferred?](#why-should-custom-networks-be-preferred) |
| 142 | [How do multiple containers share a network?](#how-do-multiple-containers-share-a-network) |
| 143 | [What is service discovery in Docker?](#what-is-service-discovery-in-docker) |
| 144 | [How do containers communicate across hosts?](#how-do-containers-communicate-across-hosts) |
| 145 | [What are overlay networks used for?](#what-are-overlay-networks-used-for) |
| 146 | [How do you troubleshoot Docker networking issues?](#how-do-you-troubleshoot-docker-networking-issues) |
| 147 | [How do you connect a running container to a network?](#how-do-you-connect-a-running-container-to-a-network) |
| 148 | [How do you disconnect a container from a network?](#how-do-you-disconnect-a-container-from-a-network) |
| 149 | [How does Docker handle IP allocation?](#how-does-docker-handle-ip-allocation) |
| 150 | [What are ingress networks?](#what-are-ingress-networks) |
| 151 | [What is network namespace isolation?](#what-is-network-namespace-isolation) |
| 152 | [How does Docker networking differ on Windows?](#how-does-docker-networking-differ-on-windows) |
| 153 | [How does Docker networking differ on Linux?](#how-does-docker-networking-differ-on-linux) |
| 154 | [What are common networking bottlenecks?](#what-are-common-networking-bottlenecks) |
| 155 | [How can Docker network performance be optimized?](#how-can-docker-network-performance-be-optimized) |
|     | **Volumes & Storage** |
| 156 | [Why are Docker volumes needed?](#why-are-docker-volumes-needed) |
| 157 | [What is the difference between volumes and bind mounts?](#what-is-the-difference-between-volumes-and-bind-mounts) |
| 158 | [What are named volumes?](#what-are-named-volumes) |
| 159 | [What are anonymous volumes?](#what-are-anonymous-volumes) |
| 160 | [What are bind mounts?](#what-are-bind-mounts) |
| 161 | [What is tmpfs storage?](#what-is-tmpfs-storage) |
| 162 | [How do you create Docker volumes?](#how-do-you-create-docker-volumes) |
| 163 | [How do you inspect Docker volumes?](#how-do-you-inspect-docker-volumes) |
| 164 | [How do you remove Docker volumes?](#how-do-you-remove-docker-volumes) |
| 165 | [How do volumes persist data?](#how-do-volumes-persist-data) |
| 166 | [How do multiple containers share a volume?](#how-do-multiple-containers-share-a-volume) |
| 167 | [What are storage drivers?](#what-are-storage-drivers) |
| 168 | [What is the overlay2 storage driver?](#what-is-the-overlay2-storage-driver) |
| 169 | [How does OverlayFS work?](#how-does-overlayfs-work) |
| 170 | [What happens when container storage is full?](#what-happens-when-container-storage-is-full) |
| 171 | [How do you back up Docker volumes?](#how-do-you-back-up-docker-volumes) |
| 172 | [How do you restore Docker volumes?](#how-do-you-restore-docker-volumes) |
| 173 | [What are common volume management practices?](#what-are-common-volume-management-practices) |
| 174 | [How do you secure Docker volumes?](#how-do-you-secure-docker-volumes) |
| 175 | [How do bind mounts impact portability?](#how-do-bind-mounts-impact-portability) |
| 176 | [What are volume plugins?](#what-are-volume-plugins) |
| 177 | [How do you migrate Docker data?](#how-do-you-migrate-docker-data) |
| 178 | [How do you troubleshoot volume issues?](#how-do-you-troubleshoot-volume-issues) |
| 179 | [What are storage performance considerations?](#what-are-storage-performance-considerations) |
| 180 | [How can volume performance be optimized?](#how-can-volume-performance-be-optimized) |
|     | **Docker Compose** |
| 181 | [What is Docker Compose?](#what-is-docker-compose) |
| 182 | [Why is Docker Compose used?](#why-is-docker-compose-used) |
| 183 | [What problems does Docker Compose solve?](#what-problems-does-docker-compose-solve) |
| 184 | [What is a compose.yaml file?](#what-is-a-composeyaml-file) |
| 185 | [What are services in Docker Compose?](#what-are-services-in-docker-compose) |
| 186 | [How do you define multiple containers in Compose?](#how-do-you-define-multiple-containers-in-compose) |
| 187 | [How do networks work in Docker Compose?](#how-do-networks-work-in-docker-compose) |
| 188 | [How do volumes work in Docker Compose?](#how-do-volumes-work-in-docker-compose) |
| 189 | [What is depends_on?](#what-is-depends_on) |
| 190 | [What are environment variables in Compose?](#what-are-environment-variables-in-compose) |
| 191 | [How do Compose profiles work?](#how-do-compose-profiles-work) |
| 192 | [How do you scale services using Compose?](#how-do-you-scale-services-using-compose) |
| 193 | [What is the difference between docker run and Compose?](#what-is-the-difference-between-docker-run-and-compose) |
| 194 | [How do you start Compose services?](#how-do-you-start-compose-services) |
| 195 | [How do you stop Compose services?](#how-do-you-stop-compose-services) |
| 196 | [How do you rebuild services in Compose?](#how-do-you-rebuild-services-in-compose) |
| 197 | [How do you override Compose files?](#how-do-you-override-compose-files) |
| 198 | [How do you debug Docker Compose applications?](#how-do-you-debug-docker-compose-applications) |
| 199 | [How do you use secrets in Compose?](#how-do-you-use-secrets-in-compose) |
| 200 | [How do health checks work in Compose?](#how-do-health-checks-work-in-compose) |
| 201 | [How do Compose networks enable service discovery?](#how-do-compose-networks-enable-service-discovery) |
| 202 | [What are Compose best practices?](#what-are-compose-best-practices) |
| 203 | [How do you deploy Compose applications?](#how-do-you-deploy-compose-applications) |
| 204 | [How do you monitor Compose services?](#how-do-you-monitor-compose-services) |
| 205 | [What are common Compose interview scenarios?](#what-are-common-compose-interview-scenarios) |
|     | **Registry & Docker Hub** |
| 206 | [What is Docker Hub?](#what-is-docker-hub-1) |
| 207 | [What is a private registry?](#what-is-a-private-registry) |
| 208 | [How do you push images to Docker Hub?](#how-do-you-push-images-to-docker-hub) |
| 209 | [How do you pull images from Docker Hub?](#how-do-you-pull-images-from-docker-hub) |
| 210 | [What is image versioning strategy?](#what-is-image-versioning-strategy) |
| 211 | [How do you authenticate with a Docker registry?](#how-do-you-authenticate-with-a-docker-registry) |
| 212 | [What are Docker Hub organizations?](#what-are-docker-hub-organizations) |
| 213 | [How do you host a private registry?](#how-do-you-host-a-private-registry) |
| 214 | [What is Harbor?](#what-is-harbor) |
| 215 | [What is Amazon ECR?](#what-is-amazon-ecr) |
| 216 | [What is Azure Container Registry (ACR)?](#what-is-azure-container-registry-acr) |
| 217 | [What is Google Artifact Registry?](#what-is-google-artifact-registry) |
| 218 | [How do you secure container registries?](#how-do-you-secure-container-registries) |
| 219 | [How do you replicate images across registries?](#how-do-you-replicate-images-across-registries) |
| 220 | [What are image retention policies?](#what-are-image-retention-policies) |
|     | **Docker Security** |
| 221 | [What are major security risks in Docker?](#what-are-major-security-risks-in-docker) |
| 222 | [How does container isolation improve security?](#how-does-container-isolation-improve-security) |
| 223 | [Why should containers not run as root?](#why-should-containers-not-run-as-root) |
| 224 | [How do you run containers as non-root users?](#how-do-you-run-containers-as-non-root-users) |
| 225 | [What are Linux capabilities in Docker?](#what-are-linux-capabilities-in-docker) |
| 226 | [How do seccomp profiles work?](#how-do-seccomp-profiles-work) |
| 227 | [What is AppArmor in Docker?](#what-is-apparmor-in-docker) |
| 228 | [What is SELinux integration in Docker?](#what-is-selinux-integration-in-docker) |
| 229 | [How do Docker secrets work?](#how-do-docker-secrets-work) |
| 230 | [How do you secure sensitive environment variables?](#how-do-you-secure-sensitive-environment-variables) |
| 231 | [How do you scan Docker images for vulnerabilities?](#how-do-you-scan-docker-images-for-vulnerabilities-1) |
| 232 | [What is Docker Content Trust?](#what-is-docker-content-trust) |
| 233 | [How does image signing work?](#how-does-image-signing-work) |
| 234 | [How do you harden Docker containers?](#how-do-you-harden-docker-containers) |
| 235 | [What are Docker security best practices?](#what-are-docker-security-best-practices) |
|     | **Docker Swarm & Orchestration** |
| 236 | [What is Docker Swarm?](#what-is-docker-swarm) |
| 237 | [How does Docker Swarm work?](#how-does-docker-swarm-work) |
| 238 | [What is a Swarm manager node?](#what-is-a-swarm-manager-node) |
| 239 | [What is a Swarm worker node?](#what-is-a-swarm-worker-node) |
| 240 | [How do you initialize a Swarm cluster?](#how-do-you-initialize-a-swarm-cluster) |
| 241 | [What are Docker services?](#what-are-docker-services) |
| 242 | [What is desired state management in Swarm?](#what-is-desired-state-management-in-swarm) |
| 243 | [How does service scaling work in Swarm?](#how-does-service-scaling-work-in-swarm) |
| 244 | [What is a rolling update in Swarm?](#what-is-a-rolling-update-in-swarm) |
| 245 | [What is service rollback in Swarm?](#what-is-service-rollback-in-swarm) |
|     | **Advanced & Scenario-Based Questions** |
| 246 | [How would you containerize a Spring Boot microservice for production?](#how-would-you-containerize-a-spring-boot-microservice-for-production) |
| 247 | [How would you reduce a 1 GB Docker image to under 200 MB?](#how-would-you-reduce-a-1-gb-docker-image-to-under-200-mb) |
| 248 | [How would you troubleshoot a container that repeatedly restarts in production?](#how-would-you-troubleshoot-a-container-that-repeatedly-restarts-in-production) |
| 249 | [How would you design a highly available Docker-based microservices platform?](#how-would-you-design-a-highly-available-docker-based-microservices-platform) |
| 250 | [How would you optimize Docker containers running on Kubernetes for performance and cost?](#how-would-you-optimize-docker-containers-running-on-kubernetes-for-performance-and-cost) |

</details>

---

## Docker Fundamentals

1. ### What is Docker and why was it created?

   Docker is an **open-source platform that automates the deployment of applications inside lightweight, portable containers**. A container bundles an application together with all its dependencies — libraries, runtime, configuration — ensuring it runs identically across development, testing, and production. Docker was created to eliminate the classic "it works on my machine" problem and to simplify application delivery in microservices and cloud environments.

   ```bash
   # Package and run an app in one command — same result on any machine
   docker run -d --name web -p 8080:80 nginx:1.27
   ```

   **[⬆ Back to Top](#table-of-contents)**

2. ### What problems does Docker solve?

   Docker addresses several long-standing software delivery pain points:

   - **Environment mismatch** — packages code and dependencies together so the runtime is identical everywhere.
   - **Isolation** — uses Linux **namespaces** and **cgroups** to keep processes and resources separate.
   - **Resource efficiency** — containers share the host kernel, so they are far lighter than virtual machines.
   - **Faster delivery** — simplifies deployment, scaling, and CI/CD pipelines.
   - **Reproducibility** — an image built once produces the same container on every host.

   **[⬆ Back to Top](#table-of-contents)**

3. ### What is containerization?

   **Containerization** is a lightweight, OS-level virtualization technique that runs applications in **isolated user spaces** on a shared host kernel. Each container has its own filesystem, process tree, and network stack (via namespaces) but does not need a full guest operating system. Resource limits are enforced by **cgroups**. This makes containers start in milliseconds and consume a fraction of the memory a VM would.

   **[⬆ Back to Top](#table-of-contents)**

4. ### How is Docker different from virtualization?

   | Aspect | Virtual Machine | Docker Container |
   | --- | --- | --- |
   | **Virtualization level** | Hardware (hypervisor) | OS-level (namespaces + cgroups) |
   | **Guest OS** | Full OS per VM | Shares host kernel |
   | **Startup time** | Seconds to minutes | Milliseconds |
   | **Size** | Gigabytes | Megabytes |
   | **Isolation** | Strong (hardware-level) | Process-level (weaker but lighter) |
   | **Density** | Few per host | Hundreds per host |

   VMs emulate hardware and run a complete OS image, offering stronger isolation. Containers share the host kernel and isolate via namespaces, trading some isolation for speed and density.

   **[⬆ Back to Top](#table-of-contents)**

5. ### What are the main components of Docker architecture?

   | Component | Role |
   | --- | --- |
   | **Docker CLI** | Client that sends API requests to the daemon over a UNIX socket; replaceable by other clients like Podman |
   | **Docker daemon (`dockerd`)** | Background service that manages images, containers, networks, and volumes |
   | **containerd** | High-level runtime that unpacks images and manages container lifecycle |
   | **runc** | Low-level OCI runtime that creates the container process |
   | **Image registry** | Stores and distributes images (e.g., Docker Hub) |

   ```bash
   # The CLI talks to dockerd, which delegates to containerd and runc
   docker info | grep -i runtime
   ```

   **[⬆ Back to Top](#table-of-contents)**

6. ### What is the difference between Docker Engine and Docker Desktop?

   **Docker Engine** is the core client-server technology that runs containers natively on Linux — it includes `dockerd`, the CLI, and the runtime. **Docker Desktop** is a GUI application for Windows and macOS that bundles Docker Engine inside a lightweight Linux VM, along with extra tooling like Kubernetes, Docker Compose, and a dashboard. On Linux you typically use Engine directly; on Windows/macOS, Desktop provides the Linux environment containers need.

   **[⬆ Back to Top](#table-of-contents)**

7. ### What is a Docker image?

   A **Docker image** is a read-only template containing a filesystem with application code, libraries, dependencies, and metadata (environment variables, entrypoint, exposed ports). Images are built as a **stack of immutable layers**, each representing a filesystem change. Images are the build-time artifact; containers are their run-time instances.

   ```bash
   # An image is identified by repository:tag and a content digest
   docker pull python:3.12-slim
   docker images python
   ```

   **[⬆ Back to Top](#table-of-contents)**

8. ### What is a Docker container?

   A **container** is a runtime instance of an image. When you run a container, Docker adds a thin **writable layer** on top of the image's read-only layers (copy-on-write) and executes a process inside isolated namespaces with cgroup-enforced resource limits. Multiple containers can be created from the same image, each with its own writable layer and runtime state.

   ```bash
   docker run -d --name app1 nginx   # container 1 from nginx image
   docker run -d --name app2 nginx   # container 2 from the SAME image
   docker ps
   ```

   **[⬆ Back to Top](#table-of-contents)**

9. ### What is Docker Hub?

   **Docker Hub** is the default public registry for hosting and distributing container images. It provides public and private repositories, official and verified images, automated builds, webhooks, organization management, and basic vulnerability scanning. When you run `docker pull nginx` without specifying a registry, Docker fetches from Docker Hub by default.

   **[⬆ Back to Top](#table-of-contents)**

10. ### What is the difference between an image and a container?

    | | Image | Container |
    | --- | --- | --- |
    | **Nature** | Static template | Running instance |
    | **Mutability** | Read-only layers | Adds a writable layer |
    | **State** | No runtime state | Has process, network, runtime state |
    | **Quantity** | One image | Many containers from one image |
    | **Analogy** | Class | Object |

    An image is like a class; a container is like an object instantiated from it.

    **[⬆ Back to Top](#table-of-contents)**

11. ### What happens internally when you run a Docker container?

    The full chain of events for `docker run`:

    1. The **CLI** sends a create/start request to `dockerd` over the UNIX socket.
    2. The daemon **pulls image layers** from a registry if they are not cached locally.
    3. **containerd** prepares the container: unpacks image layers and sets up the root filesystem snapshot.
    4. **runc** clones a process with new **namespaces** (pid, net, mnt, ipc, uts), configures **cgroups** for resource limits, mounts the union filesystem as the root, and **executes the entrypoint**.
    5. Docker attaches networking (veth pair to a bridge) and assigns an IP.

    ```bash
    docker run --rm -it alpine sh -c 'echo "PID inside container:"; ps aux'
    # The process sees PID 1 because of the PID namespace
    ```

    **[⬆ Back to Top](#table-of-contents)**

12. ### What is the role of the Docker daemon?

    The **Docker daemon (`dockerd`)** is the long-running background service that does the heavy lifting:

    - Listens for REST API requests from the CLI (or other clients).
    - **Builds images** from Dockerfiles.
    - **Manages the container lifecycle** (create, start, stop, remove).
    - Manages **networks** and **volumes**.
    - Interacts with the container runtime (`containerd`/`runc`) to actually run containers.

    It runs with elevated privileges, which is why clients can be unprivileged while the daemon performs system-level operations.

    **[⬆ Back to Top](#table-of-contents)**

13. ### What is the Docker CLI?

    The **Docker CLI** (the `docker` command) is the primary client. It translates user commands into **REST API calls** to the daemon over a UNIX domain socket (`/var/run/docker.sock`) or a TCP endpoint. Because the API is well-defined and open, the CLI can be swapped for alternative clients such as **Podman** or custom tooling built with the Docker SDK.

    ```bash
    # These two are equivalent — CLI is just a friendly wrapper over the API
    docker ps
    curl --unix-socket /var/run/docker.sock http://localhost/containers/json
    ```

    **[⬆ Back to Top](#table-of-contents)**

14. ### What are the advantages of using Docker?

    - **Portability** — "build once, run anywhere" across laptops, servers, and cloud.
    - **Consistency** — identical environments eliminate configuration drift.
    - **Isolation** — each container is sandboxed from others and the host.
    - **Efficiency** — shares the host kernel; far lighter than VMs.
    - **Scalability** — spin up/down containers quickly to match demand.
    - **Streamlined CI/CD** — images are versioned, immutable build artifacts.
    - **Rich ecosystem** — Compose, Swarm, Hub, and thousands of prebuilt images.

    **[⬆ Back to Top](#table-of-contents)**

15. ### What are the limitations of Docker?

    - **Shared kernel** — a Linux container needs a Linux kernel; you cannot run a Windows container on a Linux kernel and vice versa without virtualization.
    - **Cross-platform overhead** — on Windows/macOS, Docker runs inside a Linux VM, adding I/O and filesystem latency.
    - **Weaker isolation than VMs** — a kernel vulnerability could affect all containers; misconfiguration (`--privileged`, host mounts) increases risk.
    - **Stateful workloads** — persistent data requires careful volume management.
    - **Orchestration complexity** — large multi-host deployments need Swarm or Kubernetes.

    **[⬆ Back to Top](#table-of-contents)**

16. ### How does Docker achieve platform independence?

    A Docker image packages the **application code plus all its dependencies and a base OS userland**, but not the kernel. Containers run by interfacing with the host's kernel through the container runtime. As long as the host provides a compatible kernel and runs the Docker runtime, the container behaves identically — regardless of the underlying hardware or host distribution. This decoupling of userland from kernel is what makes images portable.

    **[⬆ Back to Top](#table-of-contents)**

17. ### What is the difference between Docker CE and Docker EE?

    **Docker Community Edition (CE)** is the free, open-source engine suitable for individual developers and small teams. **Docker Enterprise Edition (EE)** (now part of Mirantis) was a paid product adding extended security, certified infrastructure, image vulnerability scanning, role-based access control, and enterprise-grade support. Both share the same core engine but target different audiences — CE for general use, EE for regulated enterprise environments.

    **[⬆ Back to Top](#table-of-contents)**

18. ### What is the lifecycle of a Docker container?

    A container moves through several states:

    ```
    created → running → paused → running → stopped/exited → removed
    ```

    | Command | Transition |
    | --- | --- |
    | `docker create` | → created |
    | `docker start` / `docker run` | → running |
    | `docker pause` / `docker unpause` | running ↔ paused |
    | `docker stop` / `docker kill` | running → exited |
    | `docker restart` | running → running |
    | `docker rm` | exited → removed |

    ```bash
    docker create --name c1 nginx   # created
    docker start c1                 # running
    docker pause c1                 # paused
    docker unpause c1               # running
    docker stop c1                  # exited
    docker rm c1                    # removed
    ```

    **[⬆ Back to Top](#table-of-contents)**

19. ### What are common use cases of Docker?

    - **Microservices** — each service in its own container, independently deployable.
    - **CI/CD pipelines** — reproducible build and test environments.
    - **Legacy app packaging** — wrap old apps with their exact dependencies.
    - **Reproducible dev environments** — onboard developers with one command.
    - **Multi-version testing** — run app against multiple DB or language versions side by side.
    - **Machine learning** — package models with their exact library versions.
    - **Cloud deployment** — a consistent unit for Kubernetes, ECS, and serverless platforms.

    **[⬆ Back to Top](#table-of-contents)**

20. ### What are the prerequisites for running Docker?

    - A **64-bit host OS**.
    - **Linux kernel 3.10+** (modern distributions); on Windows/macOS, hardware virtualization (WSL2 or Hyper-V).
    - **Root or sudo privileges** to install and run the Engine (or rootless mode).
    - **Network connectivity** to pull images from registries.
    - Sufficient **disk space** under `/var/lib/docker` for images and containers.

    **[⬆ Back to Top](#table-of-contents)**


## Docker Architecture & Internals

21. ### Explain Docker architecture in detail

    Docker follows a **client-server architecture** with a clear separation of concerns:

    ```
    docker CLI  ──REST API (UNIX socket/TCP)──►  dockerd  ──►  containerd  ──►  runc  ──►  Linux kernel
                                                    │                                     (namespaces,
                                                    ├──► image store (layers)              cgroups,
                                                    ├──► network drivers (bridge/overlay)  OverlayFS)
                                                    └──► volume drivers
    ```

    - The **CLI** sends HTTP requests to `dockerd` over a UNIX socket or TCP.
    - **dockerd** manages images, builds, networks, volumes, and the container lifecycle.
    - **containerd** handles image pull/unpack and supervises container execution.
    - **runc** interfaces with the kernel to create containers via namespaces, cgroups, and root filesystem pivots.
    - **Registries** store images; **plugins** extend networking and storage.
    - Docker uses **union filesystems** like OverlayFS to stack read-only image layers under a writable container layer.

    **[⬆ Back to Top](#table-of-contents)**

22. ### What is the role of dockerd?

    `dockerd` is the **persistent daemon process** that is the brain of Docker. It:

    - Processes REST API requests from clients.
    - **Builds images** from Dockerfiles and the build context.
    - Manages the **lifecycle** of containers, **networks**, and **volumes**.
    - Performs orchestration tasks (in Swarm mode).
    - Delegates actual container execution to `containerd`.

    It runs as root (or in a user namespace for rootless mode), holding the system-level privileges that clients lack.

    **[⬆ Back to Top](#table-of-contents)**

23. ### What is containerd?

    **containerd** is an industry-standard, high-level **container runtime** (a CNCF graduated project). It sits between `dockerd` and `runc` and is responsible for:

    - **Pulling and unpacking** images.
    - Managing **container storage** (snapshots).
    - Supervising the **container lifecycle** (start, stop, pause, delete).
    - Managing low-level networking namespaces.

    It calls `runc` to actually create the container process. Because it's a separate standardized component, Kubernetes can use containerd directly without the Docker daemon.

    **[⬆ Back to Top](#table-of-contents)**

24. ### What is runc?

    **runc** is a **low-level container runtime** that implements the **OCI (Open Container Initiative) runtime specification**. Given a root filesystem and a configuration, it creates the container by:

    - **Cloning a process** with new namespaces.
    - Setting up **cgroups** for resource constraints.
    - Applying security profiles (seccomp, capabilities, AppArmor/SELinux).
    - Pivoting the root filesystem and **executing the entrypoint**.

    Once the container starts, `runc` exits — the container process is then just a regular Linux process supervised by containerd.

    **[⬆ Back to Top](#table-of-contents)**

25. ### How does Docker communicate with the Docker daemon?

    The CLI communicates with `dockerd` through a **REST API**, transported over a **UNIX domain socket** (`/var/run/docker.sock`) by default, or over **TCP** for remote daemons. Because the API contract is open and stable, the CLI is interchangeable with other clients (Podman, SDK-based tools, GUIs).

    ```bash
    # Talk to a remote daemon over TCP (secured with TLS)
    export DOCKER_HOST="tcp://remote-host:2376"
    docker ps
    ```

    **[⬆ Back to Top](#table-of-contents)**

26. ### What is the Docker REST API?

    The **Docker REST API** is an HTTP interface exposed by `dockerd` that lets clients perform every Docker operation programmatically — building images, creating containers, managing networks and volumes, streaming logs, etc. Libraries in many languages wrap this API.

    ```bash
    # List running containers via the raw API
    curl --unix-socket /var/run/docker.sock http://localhost/v1.44/containers/json

    # Create and start a container via the API
    curl --unix-socket /var/run/docker.sock -X POST \
      -H "Content-Type: application/json" \
      -d '{"Image":"nginx","ExposedPorts":{"80/tcp":{}}}' \
      http://localhost/v1.44/containers/create
    ```

    **[⬆ Back to Top](#table-of-contents)**

27. ### What is the purpose of Docker's client-server architecture?

    Separating the CLI (client) from `dockerd` (server) provides several benefits:

    - **Remote management** — the CLI can run on your laptop while the daemon runs on a remote server.
    - **Multiple clients** — many clients can connect to one daemon simultaneously.
    - **Privilege separation** — system-level privileges stay with the daemon; clients operate with user permissions.
    - **Extensibility** — any tool that speaks the API can drive Docker.

    **[⬆ Back to Top](#table-of-contents)**

28. ### How does Docker interact with the Linux kernel?

    Docker relies on two key kernel features plus a filesystem driver:

    - **Namespaces** — isolate what a container can *see*: `pid` (processes), `net` (network stack), `mnt` (mounts), `uts` (hostname), `ipc` (shared memory), and `user` (UID mapping).
    - **cgroups** — control what a container can *use*: CPU, memory, block I/O, and process counts.
    - **Union filesystem** (OverlayFS) — stacks image layers and provides a copy-on-write writable layer.

    ```bash
    # See the namespaces created for a container's main process
    PID=$(docker inspect --format '{{.State.Pid}}' mycontainer)
    sudo ls -l /proc/$PID/ns
    ```

    **[⬆ Back to Top](#table-of-contents)**

29. ### What is a Docker registry?

    A **registry** is a service that **stores and distributes Docker images**, supporting `push` and `pull` operations. Examples include the public **Docker Hub** and self-hosted options like **Harbor** and **JFrog Artifactory**. Registries can provide authentication, authorization, image scanning, replication, and retention policies.

    ```bash
    docker pull registry.example.com/team/app:2.1   # pull from a private registry
    docker push registry.example.com/team/app:2.1   # push to it
    ```

    **[⬆ Back to Top](#table-of-contents)**

30. ### What is the difference between local and remote registries?

    A **local (private) registry** runs on your own infrastructure (e.g., the `registry:2` container or Harbor), giving you faster pulls within the network, full control over images, and no external dependency — at the cost of maintenance. A **remote registry** like Docker Hub is externally hosted and managed for you, convenient but subject to rate limits, network latency, and external availability. Many organizations run a local registry that mirrors or caches images from remote ones.

    **[⬆ Back to Top](#table-of-contents)**

31. ### What are Docker namespaces?

    **Namespaces** partition kernel resources so each container sees only its own isolated view. The key namespaces Docker uses:

    | Namespace | Isolates |
    | --- | --- |
    | `pid` | Process IDs (container sees its own PID 1) |
    | `net` | Network interfaces, routing tables, ports |
    | `mnt` | Filesystem mount points |
    | `uts` | Hostname and domain name |
    | `ipc` | Inter-process communication (shared memory) |
    | `user` | User and group IDs (UID/GID mapping) |

    This is what makes a container *feel* like an independent machine while sharing the host kernel.

    **[⬆ Back to Top](#table-of-contents)**

32. ### What are Linux cgroups?

    **Control groups (cgroups)** limit, account for, and isolate the **resource usage** of process groups — CPU, memory, block I/O, and the number of PIDs. Docker writes to cgroup files to enforce flags like `--cpus` and `--memory`. If a container exceeds its memory limit, the kernel's **OOM killer** terminates it. **cgroups v2** unifies the hierarchy for simpler, more consistent resource management.

    ```bash
    # Limit a container to 1.5 CPUs and 512 MB of RAM
    docker run -d --cpus=1.5 --memory=512m --name limited nginx
    docker stats limited --no-stream
    ```

    **[⬆ Back to Top](#table-of-contents)**

33. ### How do namespaces and cgroups work together?

    They are **complementary**: **namespaces provide isolation** (each container gets its own view of processes, network, and filesystem), while **cgroups provide resource control** (each container is capped at a share of CPU, memory, and I/O). Together they create the illusion of an independent machine that is both sandboxed *and* prevented from starving its neighbors — all while sharing one kernel.

    **[⬆ Back to Top](#table-of-contents)**

34. ### How does Docker isolate containers?

    Docker layers multiple isolation mechanisms:

    1. **Namespaces** — isolate PIDs, network, mounts, IPC, and hostname.
    2. **cgroups** — constrain CPU, memory, and I/O so one container can't exhaust the host.
    3. **Union filesystem** — a per-container writable layer over shared read-only layers.
    4. **Capabilities** — drop most root privileges by default; add back only what's needed.
    5. **seccomp** — filter dangerous system calls.
    6. **AppArmor / SELinux** — mandatory access control profiles.

    ```bash
    # Tighten isolation: drop all capabilities, add only what's needed, no new privileges
    docker run --cap-drop=ALL --cap-add=NET_BIND_SERVICE \
      --security-opt no-new-privileges nginx
    ```

    **[⬆ Back to Top](#table-of-contents)**

35. ### What happens when the Docker daemon crashes?

    By default, **running containers keep running** because they are ordinary Linux processes managed by `containerd`/`runc`, not direct children of `dockerd`. However, you **cannot manage them** (start, stop, inspect, view logs through Docker) until the daemon restarts. When `dockerd` comes back up, it **reconnects** to the existing containers and resumes managing them. (The `live-restore` daemon option explicitly preserves this behavior across daemon upgrades.)

    **[⬆ Back to Top](#table-of-contents)**


## Installation & Setup

36. ### How do you install Docker on Linux?

    On Debian/Ubuntu, add Docker's official repository and install the packages:

    ```bash
    # 1. Install prerequisites and add Docker's GPG key
    sudo apt-get update
    sudo apt-get install -y ca-certificates curl gnupg
    sudo install -m 0755 -d /etc/apt/keyrings
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
      sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

    # 2. Add the repository
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
      https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
      sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

    # 3. Install Docker Engine
    sudo apt-get update
    sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin

    # 4. Start and enable the service
    sudo systemctl enable --now docker
    ```

    On RHEL/CentOS, use the equivalent `yum`/`dnf` repository and `dnf install docker-ce`.

    **[⬆ Back to Top](#table-of-contents)**

37. ### How do you install Docker on Windows?

    Install **Docker Desktop** from docker.com. It bundles Docker Engine inside a lightweight **WSL2** Linux VM to run Linux containers. Requirements: Windows 10/11 (Home or Pro) with WSL2 enabled and hardware virtualization turned on in BIOS. After installing, launch Docker Desktop and enable WSL2 integration for your distributions in Settings.

    ```powershell
    # Enable WSL2 first (PowerShell as Administrator)
    wsl --install
    # Then run the Docker Desktop installer and verify
    docker version
    ```

    **[⬆ Back to Top](#table-of-contents)**

38. ### How do you install Docker on macOS?

    Download **Docker Desktop for Mac** (choosing the Apple Silicon or Intel build). It runs containers inside a lightweight VM. Drag the Docker app into `/Applications`, launch it, then verify:

    ```bash
    docker version          # shows client and server versions
    docker run hello-world  # confirms the engine works end to end
    ```

    **[⬆ Back to Top](#table-of-contents)**

39. ### How do you verify a Docker installation?

    Two quick checks confirm a healthy install:

    ```bash
    # 1. Client and server (daemon) versions both respond
    docker version

    # 2. Pull and run a test container end-to-end
    docker run hello-world
    ```

    If `docker version` shows both Client and Server sections, the CLI can reach the daemon. If `hello-world` prints its welcome message, the full pull-and-run pipeline works.

    **[⬆ Back to Top](#table-of-contents)**

40. ### What is the purpose of the hello-world image?

    The **`hello-world`** image is a tiny test image that simply prints a confirmation message and exits. Running it verifies the entire pipeline end to end: the CLI reaches the daemon, the daemon pulls an image from Docker Hub, `containerd`/`runc` create a container, and output streams back to your terminal. It's the canonical "is Docker working?" smoke test.

    **[⬆ Back to Top](#table-of-contents)**

41. ### How do you configure Docker daemon settings?

    Edit `/etc/docker/daemon.json` and restart the daemon. Common settings include logging drivers, insecure registries, default address pools, and storage driver options.

    ```json
    {
      "log-driver": "json-file",
      "log-opts": { "max-size": "10m", "max-file": "3" },
      "insecure-registries": ["registry.internal:5000"],
      "default-address-pools": [{ "base": "172.30.0.0/16", "size": 24 }],
      "live-restore": true
    }
    ```

    ```bash
    sudo systemctl restart docker   # apply the changes
    ```

    **[⬆ Back to Top](#table-of-contents)**

42. ### How do you change Docker's default storage location?

    By default Docker stores everything under `/var/lib/docker`. To relocate it (e.g., to a larger disk), set `data-root` in `daemon.json`:

    ```json
    { "data-root": "/mnt/docker-data" }
    ```

    ```bash
    # Stop Docker, move existing data, then restart
    sudo systemctl stop docker
    sudo rsync -aP /var/lib/docker/ /mnt/docker-data/
    sudo systemctl start docker
    ```

    **[⬆ Back to Top](#table-of-contents)**

43. ### How do you upgrade Docker?

    Use the package manager on Linux or the GUI on Desktop:

    ```bash
    # Debian/Ubuntu
    sudo apt-get update && sudo apt-get install --only-upgrade docker-ce docker-ce-cli containerd.io

    # RHEL/CentOS
    sudo dnf update docker-ce docker-ce-cli containerd.io
    ```

    On Windows/macOS, update via Docker Desktop's "Check for updates". Enabling `live-restore` keeps containers running during the daemon restart that an upgrade triggers.

    **[⬆ Back to Top](#table-of-contents)**

44. ### How do you uninstall Docker safely?

    ```bash
    # 1. Stop and remove all containers, then prune volumes
    docker rm -f $(docker ps -aq) 2>/dev/null
    docker volume prune -f

    # 2. Uninstall the packages
    sudo apt-get purge -y docker-ce docker-ce-cli containerd.io

    # 3. Optionally remove all data (irreversible)
    sudo rm -rf /var/lib/docker /var/lib/containerd
    ```

    Remove `/var/lib/docker` only if you're certain you no longer need any images, volumes, or container data.

    **[⬆ Back to Top](#table-of-contents)**

45. ### How do you troubleshoot Docker startup issues?

    A systematic approach:

    ```bash
    # 1. Check service status and recent logs
    systemctl status docker
    sudo journalctl -u docker --no-pager -n 50

    # 2. Verify the kernel is supported
    uname -r

    # 3. Try starting the daemon in the foreground for verbose output
    sudo dockerd --debug
    ```

    Common causes: unsupported kernel, a corrupt `daemon.json` (validate the JSON), disabled virtualization on Windows/macOS, a full disk under `/var/lib/docker`, or stale state directories that need clearing.

    **[⬆ Back to Top](#table-of-contents)**


## Docker Images

46. ### What is a Docker image layer?

    An **image layer** is a read-only filesystem change produced by a single Dockerfile instruction such as `FROM`, `RUN`, or `COPY`. Each layer captures only the *delta* from the previous one and is identified by a **SHA-256 digest**. Because layers are content-addressable, identical layers are **shared across images and cached**, saving disk space and speeding up builds and pulls.

    ```dockerfile
    FROM ubuntu:22.04          # layer 1 — base
    RUN apt-get update         # layer 2 — package index
    COPY app.py /app/app.py    # layer 3 — application code
    ```

    **[⬆ Back to Top](#table-of-contents)**

47. ### How are Docker images built?

    You run `docker build` against a **Dockerfile** and a **build context** (the directory of files sent to the daemon). For each instruction, the daemon executes it in a temporary intermediate container, commits the result as a **new layer**, and feeds it to the next instruction. The final stacked set of layers becomes the tagged image.

    ```bash
    docker build -t myapp:1.0 .             # build from current directory
    docker build -t myapp:1.0 -f Dockerfile.prod .   # custom Dockerfile name
    docker buildx build --platform linux/amd64,linux/arm64 -t myapp:1.0 .  # multi-arch
    ```

    **[⬆ Back to Top](#table-of-contents)**

48. ### What is the union filesystem in Docker?

    A **union filesystem** (e.g., **overlay2**) merges multiple read-only image layers with a single writable container layer into one unified view. It uses **copy-on-write (CoW)** semantics: when a process modifies a file from a lower read-only layer, the file is first copied up into the writable layer and then changed there. Deletions are recorded with **whiteout files**. This lets many containers share the same base layers while each maintains its own changes cheaply.

    **[⬆ Back to Top](#table-of-contents)**

49. ### What is image immutability?

    **Image immutability** means once a layer is created, it is **never modified**. Any change — via `docker commit` or a new build instruction — produces a *new* layer stacked on top; the underlying layers remain untouched and content-addressed by their digest. This guarantees reproducibility (the same image digest always yields the same filesystem) and enables safe layer sharing and caching across images.

    **[⬆ Back to Top](#table-of-contents)**

50. ### How do you list Docker images?

    ```bash
    docker images                    # list all local images
    docker image ls                  # equivalent modern syntax
    docker images --filter "dangling=true"   # only untagged images
    docker images --format "{{.Repository}}:{{.Tag}} -> {{.Size}}"  # custom format
    ```

    The output shows repository, tag, image ID, creation time, and size.

    **[⬆ Back to Top](#table-of-contents)**

51. ### How do you inspect a Docker image?

    ```bash
    # Full JSON metadata: layers, env vars, entrypoint, exposed ports
    docker image inspect nginx:1.27

    # Extract a single field with a Go template
    docker image inspect --format '{{.Config.Entrypoint}}' nginx:1.27

    # Human-readable layer history
    docker history nginx:1.27
    ```

    For a detailed layer-by-layer breakdown of wasted space, third-party tools like **Dive** are popular.

    **[⬆ Back to Top](#table-of-contents)**

52. ### How do you remove Docker images?

    ```bash
    docker image rm nginx:1.27          # remove a specific image (alias: docker rmi)
    docker image prune                  # remove dangling (untagged) images
    docker image prune -a               # remove ALL unused images
    docker system prune -a              # remove unused images, containers, networks
    ```

    An image can't be removed while a container is using it unless you force it with `-f`.

    **[⬆ Back to Top](#table-of-contents)**

53. ### What is the difference between image ID and digest?

    The **image ID** is a (truncated) hash of the image's local **configuration/manifest** — what you see in `docker images`. The **digest** is the full **SHA-256 hash of the image manifest as stored in the registry**, used to verify content integrity and pull a byte-for-byte identical image. Pinning by digest (`image@sha256:...`) guarantees immutability, whereas a tag can be reassigned to a different image over time.

    ```bash
    docker images --digests nginx
    docker pull nginx@sha256:abcd1234...   # pull an exact, immutable image
    ```

    **[⬆ Back to Top](#table-of-contents)**

54. ### What are dangling images?

    **Dangling images** are layers that have **no repository tag** — typically intermediate or orphaned images left over after a rebuild reassigns a tag to a newer image. They show as `<none>:<none>` and consume disk space until cleaned.

    ```bash
    docker images --filter "dangling=true"
    docker image prune                       # removes them
    ```

    **[⬆ Back to Top](#table-of-contents)**

55. ### How do you remove unused images?

    ```bash
    docker image prune                       # dangling only (safe)
    docker image prune -a                     # all images not used by a container
    docker image prune -a --filter "until=168h"   # only images older than 7 days
    ```

    Use `-a` with care in production, as it removes any image not backing a running or stopped container.

    **[⬆ Back to Top](#table-of-contents)**

56. ### What is the difference between repository and tag?

    A **repository** is a named collection of related image versions (e.g., `nginx`). A **tag** identifies a specific version within that repository (e.g., `1.27`, `latest`). Together they form the full reference `repository:tag`. Tags are mutable labels — they can be reassigned to point at different image digests over time.

    **[⬆ Back to Top](#table-of-contents)**

57. ### What are image tags?

    **Tags** are human-readable labels for specific image versions, like `myapp:1.0` or `myapp:dev`. If you omit a tag, Docker defaults to `latest`. Tags are symbolic pointers — reassigning `myapp:1.0` to a new build doesn't change the old image's digest, only what the tag points to. Best practice is to use immutable, descriptive tags (semantic versions, commit SHAs) for reproducibility.

    ```bash
    docker tag myapp:1.0 registry.example.com/team/myapp:1.0
    docker tag myapp:1.0 myapp:stable          # one image, multiple tags
    ```

    **[⬆ Back to Top](#table-of-contents)**

58. ### Why should images be versioned?

    Pinning explicit versions ensures **reproducibility** and prevents surprise breakage from upstream changes. If you base on `python:latest`, a rebuild months later could pull a major new version with breaking changes. Pinning to `python:3.12-slim` (or even a digest) guarantees every build and deployment uses the exact same base. Always specify explicit tags in `FROM` lines and `docker run` commands.

    **[⬆ Back to Top](#table-of-contents)**

59. ### What is the latest tag and why should it be avoided?

    `latest` is **not special** — it's just the default tag name Docker applies when no tag is given. It does *not* automatically track the newest version; it points to whatever was last tagged `latest`. Relying on it in production is risky because `image:latest` may resolve to different content over time, breaking reproducibility and making rollbacks ambiguous. Use specific, immutable tags instead.

    **[⬆ Back to Top](#table-of-contents)**

60. ### What are base images?

    **Base images** are the starting layers your image builds upon, declared in the first `FROM`. They provide the OS userland, libraries, and package managers — examples are `alpine`, `ubuntu`, `debian`, and language images like `python` or `node`. Choosing a **minimal base** (Alpine or distroless) reduces image size and shrinks the attack surface.

    ```dockerfile
    FROM alpine:3.20        # ~5 MB minimal base
    # vs.
    FROM ubuntu:22.04       # ~60 MB, more packages available
    ```

    **[⬆ Back to Top](#table-of-contents)**

61. ### What are parent images?

    A **parent image** is the image referenced in your `FROM` instruction — your image inherits all of its layers, environment variables, and settings. In a multi-stage build, each stage's `FROM` defines that stage's parent. The distinction from "base image" is subtle: a base image often has no parent (built `FROM scratch`), while a parent is simply whatever your image directly extends.

    **[⬆ Back to Top](#table-of-contents)**

62. ### What is a scratch image?

    **`scratch`** is a special, completely **empty image** — no filesystem, no shell, no libraries. It's used to build truly minimal images for statically compiled binaries (common with Go and Rust). You copy in your binary and set an entrypoint; the result is tiny and has almost no attack surface.

    ```dockerfile
    FROM golang:1.22 AS build
    WORKDIR /src
    COPY . .
    RUN CGO_ENABLED=0 go build -o /app

    FROM scratch
    COPY --from=build /app /app
    ENTRYPOINT ["/app"]
    ```

    **[⬆ Back to Top](#table-of-contents)**

63. ### What is the difference between Alpine and Ubuntu images?

    | | Alpine | Ubuntu |
    | --- | --- | --- |
    | **Size** | ~5 MB | ~60–70 MB |
    | **libc** | musl libc | glibc |
    | **Package manager** | `apk` | `apt` |
    | **Compatibility** | Some glibc-dependent binaries break | Broad compatibility |
    | **Best for** | Minimal, security-focused images | Compatibility, debugging, complex deps |

    Alpine's musl libc occasionally causes subtle issues with software expecting glibc (e.g., certain Python wheels or DNS resolution edge cases). Choose Alpine for small footprint, Ubuntu/Debian for maximum compatibility.

    **[⬆ Back to Top](#table-of-contents)**

64. ### How do image layers affect storage usage?

    Layers are **shared** between images via content-addressable digests. If two images derive from the same `python:3.12-slim` base, that base is stored **once** on disk and reused. This deduplication reduces total storage and accelerates pulls (only missing layers are downloaded). Adding many small `RUN` commands, however, creates many layers and can bloat an image, so related commands are often combined.

    **[⬆ Back to Top](#table-of-contents)**

65. ### How can image size be reduced?

    - Use a **minimal base** (Alpine, distroless, or scratch).
    - Employ **multi-stage builds** to keep only runtime artifacts.
    - **Combine `RUN` commands** with `&&` to reduce layers.
    - **Clean caches** in the same layer (`apt-get clean`, `rm -rf /var/lib/apt/lists/*`).
    - Prefer **`COPY`** over `ADD`.
    - Use **`.dockerignore`** to exclude source, tests, and `.git`.

    ```dockerfile
    RUN apt-get update && apt-get install -y --no-install-recommends curl \
        && rm -rf /var/lib/apt/lists/*     # install and clean in ONE layer
    ```

    **[⬆ Back to Top](#table-of-contents)**

66. ### How do you view image history?

    ```bash
    docker history nginx:1.27               # size and command per layer
    docker history --no-trunc nginx:1.27    # full, untruncated commands
    docker history --format "{{.Size}}\t{{.CreatedBy}}" myapp:1.0
    ```

    This reveals which instructions created which layers and how much each contributes to the total size — invaluable for slimming down images.

    **[⬆ Back to Top](#table-of-contents)**

67. ### What is image caching?

    During a build, Docker **reuses cached layers** when both the instruction *and* its inputs are unchanged. As soon as one layer changes, the cache is invalidated for that layer **and all subsequent layers**. This is why ordering matters: put rarely changing instructions (dependency installs) *before* frequently changing ones (copying source code) to maximize cache hits.

    ```dockerfile
    COPY package.json .        # changes rarely — cached
    RUN npm install            # expensive — stays cached if package.json unchanged
    COPY . .                   # changes often — only this layer rebuilds
    ```

    **[⬆ Back to Top](#table-of-contents)**

68. ### How do you export and import images?

    For offline transfer, save an image to a tarball and load it elsewhere:

    ```bash
    docker save myapp:1.0 -o myapp.tar       # export image (with all layers + metadata)
    docker load -i myapp.tar                 # import on another host

    # docker export/import works on CONTAINERS (flattened, loses history)
    docker export mycontainer -o container.tar
    cat container.tar | docker import - myapp:flattened
    ```

    Note: `save`/`load` preserve layers and metadata; `export`/`import` flatten a container's filesystem and drop history.

    **[⬆ Back to Top](#table-of-contents)**

69. ### What is image digest verification?

    When you pull by **digest** (`image@sha256:...`), Docker downloads the image and verifies that the computed SHA-256 of the manifest matches the requested digest. This guarantees you received exactly the intended content — protection against tampering or accidental tag reassignment.

    ```bash
    docker pull nginx@sha256:1234abcd...     # immutable, verified pull
    ```

    **[⬆ Back to Top](#table-of-contents)**

70. ### How do you scan Docker images for vulnerabilities?

    Use a scanner to detect known CVEs in base images and dependencies:

    ```bash
    docker scout cves myapp:1.0              # Docker's built-in scanner
    trivy image myapp:1.0                    # popular open-source scanner
    grype myapp:1.0                          # Anchore's scanner
    ```

    Integrate scanning into CI to **fail builds** on critical vulnerabilities, and regularly rebuild on updated base images to pick up patches.

    **[⬆ Back to Top](#table-of-contents)**


## Containers Management

71. ### How do you create a Docker container?

    Use `docker create` to create without starting, or `docker run` to create and start in one step:

    ```bash
    # Create and start, detached, with a name and published port
    docker run -d --name web -p 8080:80 nginx:1.27

    # Create only (created state) — start it later
    docker create --name web2 nginx:1.27
    docker start web2
    ```

    Common flags: `-d` (detached), `--name`, `-p` (publish port), `-e` (env var), `-v` (volume), `--rm` (auto-remove on exit).

    **[⬆ Back to Top](#table-of-contents)**

72. ### What is the difference between docker create and docker run?

    `docker create` builds the container and leaves it in the **created** state without starting the process — useful when you want to configure or inspect before launch. `docker run` is a convenience that **combines `create` + `start`** into one command. In short: `docker run` = `docker create` followed by `docker start`.

    **[⬆ Back to Top](#table-of-contents)**

73. ### How do you start a stopped container?

    ```bash
    docker start web              # start a created or stopped container
    docker start -i web           # start and attach STDIN/STDOUT
    docker start -a web           # start and attach to view output
    ```

    The container resumes with its previous configuration and (for volumes) its persisted data.

    **[⬆ Back to Top](#table-of-contents)**

74. ### How do you stop a running container?

    ```bash
    docker stop web               # graceful: SIGTERM, then SIGKILL after timeout
    docker stop -t 30 web         # wait 30s before forcing
    ```

    `docker stop` sends **SIGTERM** to allow the app to shut down cleanly (flush buffers, close connections), then **SIGKILL** if it doesn't exit within the grace period (default 10s).

    **[⬆ Back to Top](#table-of-contents)**

75. ### What is the difference between docker stop and docker kill?

    `docker stop` is **graceful**: it sends **SIGTERM**, waits for the grace period, then sends **SIGKILL** only if the process hasn't exited. `docker kill` is **immediate**: it sends **SIGKILL** (or a signal you specify) right away, with no chance for cleanup. Use `stop` normally; use `kill` when a process is hung and ignoring SIGTERM.

    ```bash
    docker kill web                  # immediate SIGKILL
    docker kill --signal=SIGHUP web  # send a custom signal (e.g., reload)
    ```

    **[⬆ Back to Top](#table-of-contents)**

76. ### How do you restart containers?

    ```bash
    docker restart web               # stop then start
    # Configure an automatic restart policy at run time:
    docker run -d --restart=always --name web nginx
    docker run -d --restart=on-failure:5 --name worker myworker
    ```

    | Policy | Behavior |
    | --- | --- |
    | `no` | Never restart (default) |
    | `on-failure[:n]` | Restart on non-zero exit, up to *n* times |
    | `always` | Always restart (even after daemon reboot) |
    | `unless-stopped` | Like `always`, but not if you manually stopped it |

    **[⬆ Back to Top](#table-of-contents)**

77. ### How do you pause and unpause containers?

    ```bash
    docker pause web        # freeze all processes via the cgroup freezer
    docker unpause web      # resume execution
    ```

    `pause` suspends every process in the container using the cgroup **freezer** — processes are frozen in place, holding memory but consuming no CPU. This is useful for snapshotting or temporarily yielding resources without losing state.

    **[⬆ Back to Top](#table-of-contents)**

78. ### What is container state management?

    A container is always in one of several states — `created`, `running`, `paused`, `restarting`, `exited`, or `dead`. You inspect and manage these states with standard commands:

    ```bash
    docker ps                 # running containers
    docker ps -a              # all containers, any state
    docker inspect --format '{{.State.Status}}' web   # current state
    ```

    **[⬆ Back to Top](#table-of-contents)**

79. ### How do you inspect a running container?

    ```bash
    docker inspect web                       # full JSON config + network
    docker inspect --format '{{.NetworkSettings.IPAddress}}' web
    docker top web                           # processes running inside
    docker stats web --no-stream             # CPU/memory/network/IO snapshot
    ```

    `inspect` is your go-to for configuration, mounts, environment, and network details; `top` and `stats` cover live process and resource info.

    **[⬆ Back to Top](#table-of-contents)**

80. ### How do you view container logs?

    ```bash
    docker logs web                  # all stdout/stderr
    docker logs -f web               # follow (stream) live logs
    docker logs --tail 100 web       # last 100 lines
    docker logs --since 10m web      # logs from the last 10 minutes
    docker logs -t web               # with timestamps
    ```

    Logging behavior depends on the configured **logging driver** (`json-file`, `syslog`, `fluentd`, `journald`), set per-container or in `daemon.json`.

    **[⬆ Back to Top](#table-of-contents)**

81. ### How do you execute commands inside a running container?

    ```bash
    docker exec -it web /bin/bash    # interactive shell (if bash exists)
    docker exec -it web sh           # fall back to sh (Alpine)
    docker exec web ls /etc          # run a one-off command
    docker exec -u root web whoami   # run as a specific user
    ```

    `exec` starts a **new process** inside the container's namespaces — handy for debugging without disturbing the main process.

    **[⬆ Back to Top](#table-of-contents)**

82. ### What is the difference between docker attach and docker exec?

    `docker attach` connects your terminal to the container's **existing main process (PID 1)** — what you type and see goes to that primary process, and detaching incorrectly (Ctrl-C) can kill it. `docker exec` starts a **brand-new process** inside the container, independent of PID 1, so you can open a debugging shell without risking the main app. In practice, use `exec` for interactive debugging and `attach` only to interact with the primary process.

    **[⬆ Back to Top](#table-of-contents)**

83. ### How do you copy files into a container?

    ```bash
    docker cp ./config.yml web:/etc/app/config.yml      # host → container
    docker cp ./assets/ web:/usr/share/nginx/html/      # copy a directory
    ```

    `docker cp` works whether the container is running or stopped and preserves basic file metadata.

    **[⬆ Back to Top](#table-of-contents)**

84. ### How do you copy files from a container?

    ```bash
    docker cp web:/var/log/nginx/access.log ./access.log    # container → host
    docker cp web:/app/reports/ ./reports/                  # copy a directory out
    ```

    This is commonly used to extract logs, generated reports, or debug artifacts from a container.

    **[⬆ Back to Top](#table-of-contents)**

85. ### How do you rename a container?

    ```bash
    docker rename old-name new-name
    ```

    Renaming changes only the container's name; its ID, state, and data are unaffected.

    **[⬆ Back to Top](#table-of-contents)**

86. ### How do you remove containers?

    ```bash
    docker rm web                    # remove a stopped container
    docker rm -f web                 # force-remove a running container
    docker rm $(docker ps -aq)       # remove all containers
    docker container prune           # remove all stopped containers
    ```

    Use `--rm` at run time (`docker run --rm ...`) to auto-remove a container when it exits — great for one-off tasks.

    **[⬆ Back to Top](#table-of-contents)**

87. ### What are exited containers?

    **Exited containers** have finished running — either completing normally (exit code 0) or failing (non-zero). They remain on disk in the `exited` state, retaining their writable layer and logs, until you remove them. This is useful for post-mortem debugging but accumulates clutter over time.

    ```bash
    docker ps -a --filter "status=exited"
    docker inspect --format '{{.State.ExitCode}}' mycontainer
    ```

    **[⬆ Back to Top](#table-of-contents)**

88. ### How do you clean up unused containers?

    ```bash
    docker container prune                       # remove all stopped containers
    docker container prune --filter "until=24h"  # only those stopped over 24h ago
    docker system prune                          # containers + networks + dangling images
    docker system prune -a --volumes             # aggressive: also unused images + volumes
    ```

    Be cautious with `system prune -a --volumes` in production — it can delete data you still need.

    **[⬆ Back to Top](#table-of-contents)**

89. ### What happens to data when a container is deleted?

    Any data written to the container's **writable layer** is **permanently lost** when the container is removed. To persist data beyond a container's life, use **volumes** or **bind mounts**, which store data outside the writable layer.

    ```bash
    # Data in /data survives because it's on a named volume, not the writable layer
    docker run -d -v appdata:/data --name app myapp
    docker rm -f app
    docker run -d -v appdata:/data --name app2 myapp   # same data is back
    ```

    **[⬆ Back to Top](#table-of-contents)**

90. ### How do you monitor container resource usage?

    ```bash
    docker stats                     # live CPU/mem/net/IO for all containers
    docker stats web --no-stream     # one-time snapshot for one container
    docker system df                 # disk usage by images/containers/volumes
    ```

    For long-term, production-grade monitoring, integrate with **Prometheus + Grafana** (via cAdvisor or the daemon's metrics endpoint).

    **[⬆ Back to Top](#table-of-contents)**

91. ### How do you retrieve container metadata?

    ```bash
    docker inspect web                                       # full JSON
    docker inspect --format '{{.State.Status}}' web          # single field
    docker inspect --format '{{range .Mounts}}{{.Source}} -> {{.Destination}}{{"\n"}}{{end}}' web
    docker inspect --format '{{json .NetworkSettings}}' web  # subsection as JSON
    ```

    `docker inspect` with **Go template `--format`** lets you extract exactly the fields you need for scripting.

    **[⬆ Back to Top](#table-of-contents)**

92. ### How do you limit CPU usage for containers?

    ```bash
    docker run -d --cpus=1.5 myapp                   # cap at 1.5 cores
    docker run -d --cpu-shares=512 myapp             # relative weight (default 1024)
    docker run -d --cpuset-cpus="0,1" myapp          # pin to specific cores
    docker run -d --cpu-period=100000 --cpu-quota=50000 myapp  # 50% of one CPU
    ```

    The kernel's **CFS scheduler** and cgroups enforce these limits. `--cpus` is the simplest; `--cpu-shares` only matters under contention.

    **[⬆ Back to Top](#table-of-contents)**

93. ### How do you limit memory usage for containers?

    ```bash
    docker run -d --memory=512m myapp                # hard limit
    docker run -d --memory=512m --memory-swap=1g myapp   # memory + swap
    docker run -d --memory-reservation=256m myapp    # soft limit
    docker run -d --oom-kill-disable --memory=512m myapp # don't OOM-kill (risky)
    ```

    Exceeding the hard `--memory` limit triggers the kernel **OOM killer**, terminating the container. Always set memory limits in production to protect the host.

    **[⬆ Back to Top](#table-of-contents)**

94. ### How do you limit disk I/O for containers?

    ```bash
    docker run -d --device-read-bps /dev/sda:10mb myapp     # read bandwidth
    docker run -d --device-write-bps /dev/sda:5mb myapp     # write bandwidth
    docker run -d --device-read-iops /dev/sda:1000 myapp    # read IOPS
    docker run -d --device-write-iops /dev/sda:500 myapp    # write IOPS
    docker run -d --blkio-weight 500 myapp                  # relative I/O weight
    ```

    These rely on the cgroup **blkio** controller to throttle block device access — useful for noisy-neighbor isolation.

    **[⬆ Back to Top](#table-of-contents)**

95. ### How do you troubleshoot crashing containers?

    A systematic checklist:

    ```bash
    # 1. Read recent logs
    docker logs --tail 50 -f mycontainer

    # 2. Check the exit code (137 = OOM/SIGKILL, 139 = segfault)
    docker inspect --format '{{.State.ExitCode}}' mycontainer

    # 3. Look for OOM kills
    docker inspect --format '{{.State.OOMKilled}}' mycontainer
    dmesg | grep -i oom

    # 4. Watch lifecycle events in real time
    docker events --filter container=mycontainer

    # 5. Run interactively to reproduce
    docker run -it --entrypoint sh myimage
    ```

    Common culprits: misconfiguration, missing env vars/dependencies, OOM kills from low memory limits, failing health checks triggering restarts, or an entrypoint that exits immediately.

    **[⬆ Back to Top](#table-of-contents)**


## Dockerfile Instructions

96. ### What is a Dockerfile?

    A **Dockerfile** is a plain-text script of **ordered instructions** that defines how to build a Docker image. Each instruction (a keyword plus arguments) is executed by the daemon during `docker build`, producing layers that stack into the final image. It's the reproducible, version-controllable recipe for your image.

    ```dockerfile
    FROM python:3.12-slim
    WORKDIR /app
    COPY requirements.txt .
    RUN pip install --no-cache-dir -r requirements.txt
    COPY . .
    EXPOSE 8000
    CMD ["python", "app.py"]
    ```

    **[⬆ Back to Top](#table-of-contents)**

97. ### How does a Dockerfile work?

    `docker build` reads the Dockerfile **line by line**. For each instruction, Docker runs the command in a temporary intermediate container, **commits the result as a new read-only layer**, and uses that layer as the base for the next instruction. Unchanged instructions hit the build cache. The final layer stack is tagged and saved as the image.

    **[⬆ Back to Top](#table-of-contents)**

98. ### What are Dockerfile instructions?

    The common instructions and their purpose:

    | Instruction | Purpose |
    | --- | --- |
    | `FROM` | Set the base image / start a build stage |
    | `RUN` | Execute a command, creating a layer |
    | `CMD` | Default command/arguments for the container |
    | `ENTRYPOINT` | The main executable |
    | `COPY` | Copy files from build context into image |
    | `ADD` | Like COPY, plus URL fetch and tar extraction |
    | `WORKDIR` | Set the working directory |
    | `EXPOSE` | Document a listening port |
    | `ENV` | Set runtime environment variables |
    | `ARG` | Define build-time variables |
    | `LABEL` | Add metadata |
    | `VOLUME` | Declare a mount point |
    | `USER` | Set the user for subsequent steps |
    | `HEALTHCHECK` | Define a health probe |
    | `ONBUILD` | Trigger for downstream builds |

    **[⬆ Back to Top](#table-of-contents)**

99. ### What is the FROM instruction?

    **`FROM`** sets the **base image** for subsequent instructions and must be the first instruction (after optional `ARG`). The first `FROM` begins the build; additional `FROM` lines start **new stages** in a multi-stage build. You can name a stage with `AS`.

    ```dockerfile
    FROM node:20-alpine AS builder    # named stage
    FROM nginx:1.27-alpine            # second stage
    ```

    Always pin a specific tag (or digest) rather than relying on `latest`.

    **[⬆ Back to Top](#table-of-contents)**

100. ### What is the RUN instruction?

     **`RUN`** executes a command in a new layer on top of the current image and commits the result — used to install packages, compile code, or configure the filesystem. Chain related commands with `&&` and clean up in the same layer to minimize image size.

     ```dockerfile
     # Good: single layer, cache cleaned
     RUN apt-get update \
         && apt-get install -y --no-install-recommends curl ca-certificates \
         && rm -rf /var/lib/apt/lists/*
     ```

     `RUN` has two forms: **shell form** (`RUN apt-get update`, runs via `/bin/sh -c`) and **exec form** (`RUN ["executable", "arg"]`, no shell).

     **[⬆ Back to Top](#table-of-contents)**

101. ### What is the CMD instruction?

     **`CMD`** provides the **default command and/or arguments** for the running container. Only the **last `CMD`** takes effect if multiple are present. Arguments passed to `docker run` **override** `CMD`. It supports exec form (preferred) and shell form.

     ```dockerfile
     CMD ["python", "app.py"]          # exec form (preferred — no shell wrapping)
     CMD python app.py                 # shell form (runs via /bin/sh -c)
     ```

     ```bash
     docker run myimage                # runs: python app.py
     docker run myimage python test.py # CMD overridden → runs: python test.py
     ```

     **[⬆ Back to Top](#table-of-contents)**

102. ### What is the ENTRYPOINT instruction?

     **`ENTRYPOINT`** defines the container's **main executable**, which always runs and is *not* overridden by `docker run` arguments (those are appended) — unless you pass `--entrypoint`. It has two forms:

     - **Exec form** (`ENTRYPOINT ["nginx"]`) — runs directly, forwards signals properly.
     - **Shell form** (`ENTRYPOINT nginx`) — runs via `/bin/sh -c`, which can swallow signals.

     `ENTRYPOINT` is commonly paired with `CMD` to supply default arguments:

     ```dockerfile
     ENTRYPOINT ["nginx"]
     CMD ["-g", "daemon off;"]    # default args, overridable at run time
     ```

     **[⬆ Back to Top](#table-of-contents)**

103. ### What is the difference between CMD and ENTRYPOINT?

     | | CMD | ENTRYPOINT |
     | --- | --- | --- |
     | **Role** | Default arguments | Main executable |
     | **Override at run** | Replaced by `docker run` args | Args **appended**, not replaced |
     | **Full override** | N/A | Needs `--entrypoint` |
     | **Typical use** | Default behavior, easily changed | Fixed command (the container's "purpose") |

     The pattern `ENTRYPOINT ["myapp"]` + `CMD ["--default-flag"]` lets users append/replace flags while keeping `myapp` as the fixed command. Without `ENTRYPOINT`, `CMD` runs as the main process.

     ```dockerfile
     ENTRYPOINT ["python", "app.py"]
     CMD ["--port", "8000"]
     # docker run myimage              → python app.py --port 8000
     # docker run myimage --port 9000  → python app.py --port 9000
     ```

     **[⬆ Back to Top](#table-of-contents)**

104. ### What is the COPY instruction?

     **`COPY`** copies files or directories from the **build context** into the image. It's straightforward and predictable — no remote fetching, no archive extraction. It supports `--chown` to set ownership and `--from` to copy from another build stage.

     ```dockerfile
     COPY requirements.txt .
     COPY --chown=appuser:appuser ./src /app/src
     COPY --from=builder /app/dist /usr/share/nginx/html
     ```

     **[⬆ Back to Top](#table-of-contents)**

105. ### What is the ADD instruction?

     **`ADD`** is like `COPY` but with two extra behaviors: it can **auto-extract local tar archives** into the image and **download files from remote URLs**. These conveniences can cause surprising side effects and security risks, so best practice is to use `COPY` unless you specifically need ADD's features.

     ```dockerfile
     ADD app.tar.gz /opt/app/    # extracts the archive automatically
     ADD https://example.com/file.txt /tmp/   # fetches a remote file (discouraged)
     ```

     **[⬆ Back to Top](#table-of-contents)**

106. ### What is the difference between ADD and COPY?

     **`COPY`** simply copies local files/directories from the build context — explicit and safe. **`ADD`** does the same *plus* fetches remote URLs and extracts local tar archives. Because ADD's implicit behaviors (network downloads, auto-extraction) can introduce non-determinism and security concerns, the CIS Docker Benchmark and Docker's own guidance recommend **using `COPY` unless you genuinely need ADD's extra capabilities**.

     **[⬆ Back to Top](#table-of-contents)**

107. ### What is the WORKDIR instruction?

     **`WORKDIR`** sets the working directory for subsequent `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, and `ADD` instructions — equivalent to `cd`. If the directory doesn't exist, Docker creates it. Using `WORKDIR` is preferred over `RUN cd ...` because the latter doesn't persist across layers.

     ```dockerfile
     WORKDIR /usr/src/app
     COPY . .                  # copies into /usr/src/app
     RUN npm install           # runs in /usr/src/app
     ```

     **[⬆ Back to Top](#table-of-contents)**

108. ### What is the ENV instruction?

     **`ENV`** sets **environment variables** that persist in the image and are available at runtime (and to later build instructions). Useful for configuration defaults, PATH adjustments, and tuning runtime behavior.

     ```dockerfile
     ENV APP_ENV=production \
         PORT=8000 \
         PATH="/opt/app/bin:${PATH}"
     ```

     These can be overridden at run time with `docker run -e PORT=9000`.

     **[⬆ Back to Top](#table-of-contents)**

109. ### What is the ARG instruction?

     **`ARG`** defines **build-time variables** passed via `--build-arg`. Unlike `ENV`, ARG values are **not persisted** in the final image (unless you assign them to an ENV). They're ideal for parameterizing builds — version numbers, build flags, or non-sensitive configuration.

     ```dockerfile
     ARG NODE_VERSION=20
     FROM node:${NODE_VERSION}-alpine
     ARG BUILD_DATE
     LABEL build_date=$BUILD_DATE
     ```

     ```bash
     docker build --build-arg NODE_VERSION=18 --build-arg BUILD_DATE=$(date -u +%Y-%m-%d) -t myapp .
     ```

     **[⬆ Back to Top](#table-of-contents)**

110. ### What is the difference between ENV and ARG?

     | | ARG | ENV |
     | --- | --- | --- |
     | **Scope** | Build time only | Build time + runtime |
     | **Persisted in image** | No | Yes |
     | **Set via** | `--build-arg` | `ENV` or `docker run -e` |
     | **Use for** | Build parameters (versions, flags) | Runtime configuration |

     Use `ARG` for values needed only during the build (not exposed in the running container), and `ENV` for configuration the application reads at runtime. Note: neither should hold true secrets — use build secrets or a secrets manager instead.

     **[⬆ Back to Top](#table-of-contents)**

111. ### What is the EXPOSE instruction?

     **`EXPOSE`** **documents** which port(s) the container listens on — it does *not* actually publish them to the host. It serves as metadata and enables `docker run -P` to auto-map exposed ports to random host ports.

     ```dockerfile
     EXPOSE 8080
     EXPOSE 8080/tcp 5353/udp
     ```

     ```bash
     docker run -P myimage    # publishes EXPOSEd ports to random host ports
     docker port mycontainer  # see the actual mapping
     ```

     **[⬆ Back to Top](#table-of-contents)**

112. ### What is the USER instruction?

     **`USER`** sets the UID (and optionally GID) that subsequent instructions and the container's main process run as. Running as a **non-root user** is a key security practice that limits the blast radius of a container escape.

     ```dockerfile
     RUN addgroup -S app && adduser -S -G app appuser
     USER appuser
     WORKDIR /home/appuser
     CMD ["./start.sh"]
     ```

     **[⬆ Back to Top](#table-of-contents)**

113. ### What is the LABEL instruction?

     **`LABEL`** attaches **metadata** to an image as key-value pairs — maintainer, version, description, source repo, etc. Labels are queryable and useful for automation, filtering, and provenance tracking. The OCI image spec defines standard label keys.

     ```dockerfile
     LABEL maintainer="team@example.com" \
           org.opencontainers.image.version="1.2.3" \
           org.opencontainers.image.source="https://github.com/team/app"
     ```

     ```bash
     docker images --filter "label=org.opencontainers.image.version=1.2.3"
     ```

     **[⬆ Back to Top](#table-of-contents)**

114. ### What is the VOLUME instruction?

     **`VOLUME`** declares a mount point whose data should persist outside the container's writable layer. At run time, if no host path or named volume is supplied, Docker creates an **anonymous volume** there. It's commonly used for databases and data directories.

     ```dockerfile
     VOLUME /var/lib/mysql
     ```

     Note: declaring `VOLUME` means writes to that path won't be committed to image layers in later build steps, so set up data *before* the `VOLUME` declaration.

     **[⬆ Back to Top](#table-of-contents)**

115. ### What is the HEALTHCHECK instruction?

     **`HEALTHCHECK`** defines a command Docker runs periodically to determine if the container is **healthy** or **unhealthy**. The result appears in `docker ps` and can drive orchestration decisions (e.g., Compose `depends_on: condition: service_healthy`).

     ```dockerfile
     HEALTHCHECK --interval=30s --timeout=3s --retries=3 --start-period=10s \
       CMD curl -f http://localhost:8080/health || exit 1
     ```

     ```bash
     docker inspect --format '{{.State.Health.Status}}' web   # healthy / unhealthy / starting
     ```

     **[⬆ Back to Top](#table-of-contents)**

116. ### What is the ONBUILD instruction?

     **`ONBUILD`** registers a **trigger instruction** that executes only when the image is used as a base (`FROM`) in a *downstream* Dockerfile. It's used to build reusable "builder" base images that automatically inject `COPY`/`RUN` steps into child builds.

     ```dockerfile
     # In a base image
     ONBUILD COPY . /app/src
     ONBUILD RUN make -C /app/src
     # When a child does `FROM this-base`, the COPY and RUN fire automatically
     ```

     Use sparingly — the hidden behavior can confuse downstream users.

     **[⬆ Back to Top](#table-of-contents)**

117. ### How does the Docker build context work?

     The **build context** is the set of files (the directory you pass to `docker build`) that the CLI **sends to the daemon**. Only files inside the context can be referenced by `COPY` and `ADD`. A large context (e.g., including `node_modules` or `.git`) slows builds and wastes bandwidth, so trim it with `.dockerignore`.

     ```bash
     docker build -t myapp .              # context = current directory
     docker build -t myapp ./backend      # context = ./backend only
     docker build -t myapp https://github.com/user/repo.git   # remote context
     ```

     **[⬆ Back to Top](#table-of-contents)**

118. ### What is .dockerignore?

     **`.dockerignore`** works like `.gitignore`: it lists files and directories to **exclude from the build context**, keeping builds fast and images lean. Excluding `.git`, `node_modules`, secrets, and test data prevents them from being sent to the daemon and accidentally copied into the image.

     ```
     .git
     node_modules
     *.log
     .env
     **/__pycache__
     Dockerfile
     .dockerignore
     ```

     **[⬆ Back to Top](#table-of-contents)**

119. ### How do you optimize Dockerfiles?

     - **Order from least to most volatile** — put dependency installs before copying source so the cache survives code changes.
     - **Combine `RUN` commands** and clean caches in the same layer.
     - **Use minimal base images** (Alpine, slim, distroless).
     - **Use multi-stage builds** to drop build tools from the final image.
     - **Prefer `COPY`** over `ADD`.
     - **Use `.dockerignore`** to shrink the context.
     - **Pin versions** for reproducibility.

     ```dockerfile
     COPY package*.json ./       # rarely changes — stays cached
     RUN npm ci --omit=dev       # expensive — cached unless deps change
     COPY . .                    # changes often — only this rebuilds
     ```

     **[⬆ Back to Top](#table-of-contents)**

120. ### What are Dockerfile best practices?

     - Keep images **minimal and secure** — remove build tools, run as **non-root**.
     - **Pin versions** in `FROM` lines (avoid `latest`).
     - Use **`COPY` instead of `ADD`** unless you need ADD's features.
     - **Combine commands** with `&&` to reduce layers and clean caches.
     - Add **`HEALTHCHECK`** and handle signals properly (exec form).
     - Use **`.dockerignore`** to exclude unnecessary files.
     - **Document** ports and data dirs with `EXPOSE` and `VOLUME`.
     - Leverage **multi-stage builds** and the **build cache**.
     - Use **`--no-install-recommends`** and **`--no-cache-dir`** to avoid bloat.

     **[⬆ Back to Top](#table-of-contents)**

121. ### What is a multi-stage Docker build?

     A **multi-stage build** uses multiple `FROM` instructions in one Dockerfile. Early stages compile or build artifacts using full toolchains; the final stage copies only the resulting artifacts into a minimal runtime image. This keeps build dependencies out of the final image, dramatically reducing size and attack surface.

     ```dockerfile
     # Stage 1: build
     FROM golang:1.22 AS build
     WORKDIR /src
     COPY . .
     RUN CGO_ENABLED=0 go build -o /bin/app

     # Stage 2: minimal runtime
     FROM gcr.io/distroless/static
     COPY --from=build /bin/app /app
     ENTRYPOINT ["/app"]
     ```

     **[⬆ Back to Top](#table-of-contents)**

122. ### Why are multi-stage builds important?

     They deliver **small, secure production images** by separating build-time concerns from runtime. Benefits: the final image excludes compilers, build caches, and source code (smaller size, **reduced attack surface**); the entire build is consolidated in one Dockerfile (no external scripts); and you can target individual stages for testing. A 1 GB build image can shrink to tens of MB at runtime.

     **[⬆ Back to Top](#table-of-contents)**

123. ### How do build arguments work?

     Define variables with `ARG` and supply values at build time via `--build-arg`. They customize builds (versions, feature flags) without editing the Dockerfile, and are not persisted in the final image unless promoted to `ENV`.

     ```dockerfile
     ARG APP_VERSION=1.0.0
     ARG ENVIRONMENT=production
     RUN echo "Building version ${APP_VERSION} for ${ENVIRONMENT}"
     ENV APP_VERSION=${APP_VERSION}   # promote to runtime if needed
     ```

     ```bash
     docker build --build-arg APP_VERSION=2.1.0 --build-arg ENVIRONMENT=staging -t myapp .
     ```

     **[⬆ Back to Top](#table-of-contents)**

124. ### How can Docker build time be reduced?

     - **Maximize cache hits** — order instructions least-to-most volatile.
     - **Minimize the build context** with `.dockerignore`.
     - **Combine `apt-get update && install`** in one `RUN`.
     - **Use multi-stage builds** and `--target` to build only what you need.
     - **Copy only necessary files** before expensive steps.
     - **Use BuildKit** (`DOCKER_BUILDKIT=1`) for parallel stage builds and cache mounts.

     ```dockerfile
     # syntax=docker/dockerfile:1
     RUN --mount=type=cache,target=/root/.cache/pip \
         pip install -r requirements.txt    # BuildKit cache mount persists across builds
     ```

     **[⬆ Back to Top](#table-of-contents)**

125. ### How do you debug Dockerfile issues?

     ```bash
     # 1. See plain, full output from each step
     docker build --progress=plain -t myapp .

     # 2. Force a clean build to rule out stale cache
     docker build --no-cache -t myapp .

     # 3. Build up to a specific stage and inspect it
     docker build --target build -t myapp:debug .
     docker run -it myapp:debug sh

     # 4. Inspect an intermediate layer interactively
     docker run -it <intermediate-image-id> sh
     ```

     Add temporary `RUN echo`/`RUN ls -la` steps to print state, and use BuildKit's plain progress to see exactly which instruction fails.

     **[⬆ Back to Top](#table-of-contents)**


## Docker Networking

126. ### How does Docker networking work?

     Each container gets its own **network namespace** with isolated interfaces and routing tables. Docker creates a **virtual Ethernet (veth) pair**: one end inside the container, the other attached to a host **bridge** (e.g., `docker0`). It assigns the container an IP from the network's subnet and sets up **NAT/iptables** rules so the container can reach external networks and (with port publishing) be reached from outside.

     ```bash
     docker network ls                  # list networks
     docker network inspect bridge      # see subnet, gateway, connected containers
     ```

     **[⬆ Back to Top](#table-of-contents)**

127. ### What is the default bridge network?

     Docker automatically creates a default **`bridge`** network (backed by the `docker0` Linux bridge). Containers attached to it get private IPs and can talk to each other **by IP** (but **not by name** — the default bridge lacks automatic DNS). Outbound traffic is NATed through the host. For service discovery by name, use a **user-defined** bridge instead.

     **[⬆ Back to Top](#table-of-contents)**

128. ### What is a bridge network?

     A **bridge network** is a private, host-internal network implemented via a Linux bridge device, with containers connected through veth pairs. **User-defined bridge networks** (created with `docker network create`) are preferred because they provide **automatic DNS-based service discovery** — containers resolve each other by name — plus better isolation and configurable subnets.

     ```bash
     docker network create --driver bridge mynet
     docker run -d --network mynet --name db postgres:16
     docker run -d --network mynet --name app myapp   # 'app' can reach 'db' by name
     ```

     **[⬆ Back to Top](#table-of-contents)**

129. ### What is a host network?

     The **host network** (`--network host`) **removes network isolation** — the container shares the host's network stack directly, with no separate namespace and no NAT. This improves performance (no bridge/NAT overhead) but means the container binds host ports directly, so **only one container can use a given port**, and there's less isolation. Useful for high-throughput or latency-sensitive workloads. (Linux only; behaves differently on Docker Desktop.)

     ```bash
     docker run -d --network host nginx   # nginx binds host's port 80 directly
     ```

     **[⬆ Back to Top](#table-of-contents)**

130. ### What is a none network?

     The **`none`** network (`--network none`) gives the container its own network namespace **with no interfaces** except loopback — complete network isolation. It's used for batch jobs that need no connectivity or where networking is configured manually afterward.

     ```bash
     docker run --network none alpine ip addr   # only 'lo' present
     ```

     **[⬆ Back to Top](#table-of-contents)**

131. ### What is an overlay network?

     An **overlay network** spans **multiple Docker hosts**, letting containers on different machines communicate as if on one LAN. It encapsulates traffic in **VXLAN** tunnels and is used with **Swarm** (and conceptually by Kubernetes CNIs). Essential for multi-host orchestration and cross-node service discovery.

     ```bash
     docker network create -d overlay --attachable my_overlay
     docker service create --network my_overlay --name web nginx
     ```

     **[⬆ Back to Top](#table-of-contents)**

132. ### What is a macvlan network?

     A **macvlan network** assigns each container its **own MAC address**, making it appear as a **physical device directly on the host's LAN** with an IP from that physical network. This enables direct L2 connectivity (no NAT) — useful for legacy apps or network appliances that must be first-class citizens on the physical network.

     ```bash
     docker network create -d macvlan \
       --subnet=192.168.1.0/24 --gateway=192.168.1.1 \
       -o parent=eth0 mymacvlan
     docker run -d --network mymacvlan --ip=192.168.1.50 myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

133. ### How do containers communicate with each other?

     On a **user-defined network**, containers reach each other by **container name** (Docker's embedded DNS resolves names to IPs). On the default bridge, only IP-based communication works. For cross-host communication, use an **overlay** network or **macvlan**.

     ```bash
     docker network create appnet
     docker run -d --network appnet --name redis redis:7
     docker run -it --network appnet alpine ping redis   # resolves by name
     ```

     **[⬆ Back to Top](#table-of-contents)**

134. ### How does DNS resolution work in Docker?

     Docker runs an **embedded DNS server** (at `127.0.0.11` inside containers) on every user-defined network. Containers query it to resolve **service/container names** to their current IPs — no manual `/etc/hosts` editing needed. You can override upstream DNS with `--dns`, set search domains with `--dns-search`, and add static entries with `--add-host`.

     ```bash
     docker run --dns 8.8.8.8 --add-host db:10.0.0.5 myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

135. ### What is port mapping?

     **Port mapping (publishing)** exposes a container's internal port on the host so external clients can reach it. Docker sets up **iptables NAT** rules to forward host:port traffic to container:port.

     ```bash
     docker run -d -p 8080:80 nginx          # host 8080 → container 80
     docker run -d -p 127.0.0.1:8080:80 nginx # bind only to localhost
     docker run -d -p 80:80/udp myapp         # UDP mapping
     docker run -d -P nginx                    # publish all EXPOSEd ports to random host ports
     ```

     **[⬆ Back to Top](#table-of-contents)**

136. ### What is the difference between EXPOSE and port publishing?

     **`EXPOSE`** (in the Dockerfile) is **documentation only** — it declares which ports the container listens on but does not make them reachable from the host. **Publishing** (`-p` or `-P` at run time) actually binds host ports to container ports via NAT. In short: `EXPOSE` informs; `-p`/`-P` connects.

     **[⬆ Back to Top](#table-of-contents)**

137. ### How do you publish container ports?

     ```bash
     docker run -d -p 8080:80 nginx           # explicit host:container mapping
     docker run -d -p 80 nginx                # random host port → container 80
     docker run -d -P nginx                    # publish all EXPOSEd ports randomly
     docker port mycontainer                   # show actual mappings
     ```

     In Compose, use the `ports:` key. Bind to a specific interface (`-p 127.0.0.1:8080:80`) to restrict access.

     **[⬆ Back to Top](#table-of-contents)**

138. ### What is network isolation?

     **Network isolation** means each container has its own network namespace, so containers cannot see each other's interfaces or traffic unless they share a network. You can strengthen isolation by placing services on **separate user-defined networks**, disabling inter-container communication (`--icc=false` on the daemon), or using the `internal` flag to block external access.

     ```bash
     docker network create --internal backend   # no external connectivity
     ```

     **[⬆ Back to Top](#table-of-contents)**

139. ### How do you inspect Docker networks?

     ```bash
     docker network ls                    # list all networks
     docker network inspect mynet         # subnet, gateway, connected containers
     docker network inspect --format '{{range .Containers}}{{.Name}} {{.IPv4Address}}{{"\n"}}{{end}}' mynet
     docker network prune                 # remove unused networks
     ```

     `inspect` is essential for debugging connectivity — it shows which containers are attached and their assigned IPs.

     **[⬆ Back to Top](#table-of-contents)**

140. ### How do you create custom networks?

     ```bash
     docker network create --driver bridge mynet
     docker network create --driver bridge \
       --subnet=172.20.0.0/16 --gateway=172.20.0.1 customnet
     docker run -d --network mynet --name app myapp
     ```

     Custom (user-defined) bridge networks provide automatic DNS and isolation. In Compose, networks are created automatically for each project.

     **[⬆ Back to Top](#table-of-contents)**

141. ### Why should custom networks be preferred?

     User-defined bridge networks offer key advantages over the default bridge:

     - **Automatic DNS resolution** — containers reach each other by name, not just IP.
     - **Better isolation** — only containers on the same network can communicate.
     - **Configurable subnets/gateways** — full control over addressing.
     - **Dynamic attach/detach** — connect and disconnect containers at runtime without restart.

     **[⬆ Back to Top](#table-of-contents)**

142. ### How do multiple containers share a network?

     Create a network and attach each container with `--network`. They then share a namespace-level network and can communicate by name.

     ```bash
     docker network create sharednet
     docker run -d --network sharednet --name api myapi
     docker run -d --network sharednet --name worker myworker
     # In Compose, all services join the project's default network automatically
     ```

     A container can also be attached to multiple networks with repeated `docker network connect`.

     **[⬆ Back to Top](#table-of-contents)**

143. ### What is service discovery in Docker?

     **Service discovery** is the automatic mapping of service/container names to current IP addresses. On user-defined networks, Docker's **embedded DNS** handles this. In **Swarm**, an internal DNS resolves a service name to a **virtual IP (VIP)** that load-balances across all healthy task replicas — clients just use the service name and Swarm routes to a backend.

     **[⬆ Back to Top](#table-of-contents)**

144. ### How do containers communicate across hosts?

     Use an **overlay network** (with Swarm or a Kubernetes CNI). The overlay driver encapsulates container traffic in **VXLAN** packets and routes them between hosts over the physical network, so containers on different machines communicate using their overlay IPs/names as if on the same LAN.

     ```bash
     # On a Swarm: containers on this overlay span all nodes
     docker network create -d overlay --attachable cross_host_net
     ```

     **[⬆ Back to Top](#table-of-contents)**

145. ### What are overlay networks used for?

     Overlay networks enable **multi-host container communication**, **service discovery**, and **load balancing** across a cluster. They are required for Docker Swarm services and are the conceptual basis for Kubernetes pod networking. They also support encryption of inter-host traffic (`--opt encrypted`).

     **[⬆ Back to Top](#table-of-contents)**

146. ### How do you troubleshoot Docker networking issues?

     ```bash
     # 1. Check network config and attached containers
     docker network inspect mynet

     # 2. Test connectivity from inside a container
     docker exec -it app ping db
     docker exec -it app curl http://db:5432
     docker exec -it app nslookup db

     # 3. Verify published ports and host iptables
     docker port app
     sudo iptables -t nat -L -n | grep DOCKER

     # 4. Check for port conflicts
     sudo ss -tulpn | grep 8080
     ```

     Common issues: containers on different networks, missing/wrong port publishing, port conflicts, DNS failures (default bridge), or MTU mismatches on overlays.

     **[⬆ Back to Top](#table-of-contents)**

147. ### How do you connect a running container to a network?

     ```bash
     docker network connect mynet mycontainer            # attach to an additional network
     docker network connect --ip 172.20.0.10 mynet mycontainer  # with a static IP
     docker inspect --format '{{json .NetworkSettings.Networks}}' mycontainer
     ```

     A container can belong to multiple networks simultaneously, which is useful for bridging tiers (e.g., a proxy on both frontend and backend networks).

     **[⬆ Back to Top](#table-of-contents)**

148. ### How do you disconnect a container from a network?

     ```bash
     docker network disconnect mynet mycontainer
     docker network disconnect -f mynet mycontainer   # force, even if running
     ```

     Disconnecting removes the container's interface on that network; it retains connectivity on any other networks it's still attached to.

     **[⬆ Back to Top](#table-of-contents)**

149. ### How does Docker handle IP allocation?

     For **bridge** networks, Docker's built-in IPAM assigns each container an IP from the network's subnet automatically (you can specify custom subnets, gateways, and IP ranges, or pin a static IP with `--ip`). For **overlay** networks, IPs come from the overlay subnet and are coordinated across all nodes in the cluster so addresses don't collide.

     ```bash
     docker network create --subnet=10.10.0.0/24 --ip-range=10.10.0.128/25 mynet
     docker run --network mynet --ip 10.10.0.200 myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

150. ### What are ingress networks?

     In **Swarm mode**, the **ingress network** is a special overlay that implements the **routing mesh** for published service ports. A request to *any* node's published port is routed through the ingress load balancer to a healthy task replica — even if that replica runs on a different node. This gives transparent, cluster-wide load balancing for published services.

     **[⬆ Back to Top](#table-of-contents)**

151. ### What is network namespace isolation?

     Each container runs in its own **network namespace**, which contains a private set of network interfaces, routing tables, iptables rules, and port space. This prevents containers from seeing or interfering with each other's network stack by default. It's the kernel feature that makes per-container IPs and isolated networking possible.

     **[⬆ Back to Top](#table-of-contents)**

152. ### How does Docker networking differ on Windows?

     On Windows, **Docker Desktop** runs Linux containers inside a **WSL2 (or Hyper-V) Linux VM**, so Linux containers use the VM's networking and reach the host via NAT — published ports are forwarded from Windows to the VM. **Native Windows containers** use Windows networking constructs like **HNS (Host Networking Service)** and NAT networks rather than the Linux bridge driver. The `host` network mode behaves differently than on native Linux.

     **[⬆ Back to Top](#table-of-contents)**

153. ### How does Docker networking differ on Linux?

     On **Linux**, Docker uses **native kernel networking** — real bridge, overlay, and macvlan drivers, with direct iptables/NAT manipulation. There's no intermediary VM, so networking is faster and offers the full range of drivers and options. `host` mode truly shares the host stack. This is why Linux is the reference platform for Docker networking.

     **[⬆ Back to Top](#table-of-contents)**

154. ### What are common networking bottlenecks?

     | Bottleneck | Cause |
     | --- | --- |
     | **NAT throughput** | All bridge traffic funneled through host NAT |
     | **Overlay overhead** | VXLAN encapsulation adds CPU and latency |
     | **DNS resolution delays** | Slow or misconfigured embedded/upstream DNS |
     | **Port binding conflicts** | Multiple services contend for the same host port |
     | **Connection limits** | Many concurrent connections exhaust conntrack table |
     | **MTU mismatch** | Wrong MTU on overlays causes fragmentation |

     **[⬆ Back to Top](#table-of-contents)**

155. ### How can Docker network performance be optimized?

     - Use **host networking** for latency-critical services (accepting reduced isolation).
     - **Tune MTU** on overlay networks to avoid fragmentation (`--opt com.docker.network.driver.mtu`).
     - Use **macvlan** for direct L2 access without NAT.
     - **Avoid unnecessary NAT** by co-locating chatty services on the same network.
     - Ensure sufficient **CPU/IO** for VXLAN encapsulation on overlays.
     - Increase **conntrack limits** for high-connection workloads.

     **[⬆ Back to Top](#table-of-contents)**


## Volumes & Storage

156. ### Why are Docker volumes needed?

     A container's **writable layer is ephemeral** — when the container is removed, its data is gone. **Volumes** store persistent or shared data **outside** that layer, so it survives container deletion, recreation, and upgrades. They're essential for databases, user uploads, logs, and any state that must outlive a container.

     ```bash
     docker volume create pgdata
     docker run -d -v pgdata:/var/lib/postgresql/data postgres:16
     # The database survives even if the container is removed and recreated
     ```

     **[⬆ Back to Top](#table-of-contents)**

157. ### What is the difference between volumes and bind mounts?

     | | Volume | Bind Mount |
     | --- | --- | --- |
     | **Managed by** | Docker (`/var/lib/docker/volumes`) | You (any host path) |
     | **Portability** | High — host-path-independent | Low — depends on host layout |
     | **Isolation** | Isolated from host filesystem | Direct host access |
     | **Use case** | Production data persistence | Local dev (live source mounting) |
     | **CLI management** | `docker volume` commands | None (just a path) |

     **Volumes** are Docker-managed, portable, and the recommended default. **Bind mounts** map an exact host directory into the container — powerful for development (live code reload) but tied to host structure and able to shadow existing container files, so use carefully (often read-only).

     **[⬆ Back to Top](#table-of-contents)**

158. ### What are named volumes?

     **Named volumes** have an explicit name and **persist independently** of any container. They're created with `docker volume create` (or implicitly by Compose) and can be mounted into multiple containers. They survive `docker rm` and are only deleted when you explicitly remove them.

     ```bash
     docker volume create appdata
     docker run -d -v appdata:/data --name app1 myapp
     docker run -d -v appdata:/shared --name app2 myapp   # shares the same data
     ```

     **[⬆ Back to Top](#table-of-contents)**

159. ### What are anonymous volumes?

     **Anonymous volumes** are created automatically — without a chosen name — when a container uses a `VOLUME` instruction or a `-v /path` mount with no source name. Docker assigns them a random hash ID. They persist until the container is removed (or are removed immediately if you used `--rm`). Because they're hard to track, named volumes are preferred for anything you need to manage.

     ```bash
     docker run -d -v /app/cache myapp   # creates an anonymous volume for /app/cache
     docker volume ls -f dangling=true   # find orphaned anonymous volumes
     ```

     **[⬆ Back to Top](#table-of-contents)**

160. ### What are bind mounts?

     A **bind mount** maps a specific **host file or directory** into the container at a chosen path. Changes are reflected both ways in real time. Typical uses: mounting source code for live-reload during development, sharing config files, or persisting logs to a known host location.

     ```bash
     docker run -d -v /home/dev/src:/app/src myapp           # live source
     docker run -d -v /etc/myapp/config.yml:/app/config.yml:ro myapp  # read-only config
     docker run -d --mount type=bind,source="$(pwd)",target=/app myapp # explicit syntax
     ```

     **[⬆ Back to Top](#table-of-contents)**

161. ### What is tmpfs storage?

     A **tmpfs mount** stores data in the host's **RAM**, never touching disk. It's fast and ephemeral — data vanishes when the container stops. Ideal for sensitive data (secrets you don't want persisted) or high-speed scratch space.

     ```bash
     docker run -d --tmpfs /tmp:rw,size=64m myapp
     docker run -d --mount type=tmpfs,destination=/cache,tmpfs-size=100m myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

162. ### How do you create Docker volumes?

     ```bash
     docker volume create myvol
     docker volume create --driver local \
       --opt type=nfs --opt o=addr=192.168.1.1,rw \
       --opt device=:/path/to/dir nfsvol   # NFS-backed volume
     ```

     In Compose, declare volumes under the top-level `volumes:` key. Volumes are also created implicitly the first time they're referenced in a `-v` mount.

     **[⬆ Back to Top](#table-of-contents)**

163. ### How do you inspect Docker volumes?

     ```bash
     docker volume ls                       # list volumes
     docker volume inspect myvol            # mountpoint, driver, options, labels
     docker volume inspect --format '{{.Mountpoint}}' myvol   # just the host path
     ```

     `inspect` reveals the on-disk location (`/var/lib/docker/volumes/myvol/_data`), driver, and any driver options.

     **[⬆ Back to Top](#table-of-contents)**

164. ### How do you remove Docker volumes?

     ```bash
     docker volume rm myvol                 # remove a specific volume
     docker volume prune                    # remove all unused volumes
     docker volume prune -a                 # include named volumes not in use
     docker rm -v mycontainer               # remove container AND its anonymous volumes
     ```

     A volume can't be removed while a container is using it. Prune carefully — volume data is unrecoverable once deleted.

     **[⬆ Back to Top](#table-of-contents)**

165. ### How do volumes persist data?

     Volumes live **outside the container's writable layer**, in Docker's managed storage area (or on external storage via a driver). Because they're decoupled from container lifecycle, removing or recreating a container **does not** delete the volume's data (unless you use `--rm` with anonymous volumes or explicitly prune). This decoupling is the foundation of stateful containerized applications.

     **[⬆ Back to Top](#table-of-contents)**

166. ### How do multiple containers share a volume?

     Mount the **same named volume** into multiple containers. Data written by one is immediately visible to the others.

     ```bash
     docker volume create shared
     docker run -d -v shared:/app/data --name writer myapp
     docker run -d -v shared:/backup/data --name backup busybox
     # 'backup' sees everything 'writer' writes to /app/data
     ```

     Coordinate file permissions and avoid concurrent writes to the same file unless the application handles locking.

     **[⬆ Back to Top](#table-of-contents)**

167. ### What are storage drivers?

     **Storage drivers** implement the union filesystem for image layers and the container's writable layer. Options include **overlay2** (default on modern kernels), `fuse-overlayfs` (rootless), `btrfs`, `zfs`, `aufs` (legacy), and `devicemapper` (legacy). They differ in performance, CoW implementation, and kernel requirements; **overlay2** is the recommended, widely used default.

     ```bash
     docker info | grep "Storage Driver"
     ```

     **[⬆ Back to Top](#table-of-contents)**

168. ### What is the overlay2 storage driver?

     **overlay2** is the **preferred storage driver** on modern Linux kernels. It uses the kernel's **OverlayFS** to stack image layers and implements **copy-on-write** efficiently, with lower inode consumption and better performance than older drivers like `aufs` or `devicemapper`. It works best on `ext4` or `xfs` (with `ftype=1`).

     **[⬆ Back to Top](#table-of-contents)**

169. ### How does OverlayFS work?

     OverlayFS merges a **`lowerdir`** (read-only image layers) and an **`upperdir`** (the writable container layer) into a single unified **`merged`** view:

     - **Read** — served from the upper layer if present, otherwise from the lower layers.
     - **Write/modify** — the file is **copied up** from lower to upper (copy-on-write), then changed.
     - **Delete** — recorded as a **whiteout file** in the upper layer that masks the lower copy.

     This lets many containers share read-only base layers while each keeps only its own changes.

     **[⬆ Back to Top](#table-of-contents)**

170. ### What happens when container storage is full?

     When the disk backing `/var/lib/docker` fills up, **writes fail** — applications hit "no space left on device" errors, containers may crash, and new pulls/builds fail. Mitigations: monitor disk usage (`docker system df`), prune unused images/containers/volumes, put `/var/lib/docker` on a dedicated partition with ample space, and set log rotation to prevent runaway log growth.

     ```bash
     docker system df                 # see space used
     docker system prune -a --volumes # reclaim space (careful!)
     ```

     **[⬆ Back to Top](#table-of-contents)**

171. ### How do you back up Docker volumes?

     Mount the volume into a temporary container and `tar` it to a host path:

     ```bash
     docker run --rm \
       -v mydata:/data \
       -v "$(pwd)":/backup \
       busybox tar czf /backup/mydata.tar.gz -C /data .
     ```

     This produces `mydata.tar.gz` on the host containing the volume's contents — portable and restorable anywhere.

     **[⬆ Back to Top](#table-of-contents)**

172. ### How do you restore Docker volumes?

     Create a fresh volume and extract the backup archive into it via a helper container:

     ```bash
     docker volume create mydata
     docker run --rm \
       -v mydata:/data \
       -v "$(pwd)":/backup \
       busybox sh -c "cd /data && tar xzf /backup/mydata.tar.gz"
     ```

     The new volume now mirrors the backed-up state and can be mounted into your application container.

     **[⬆ Back to Top](#table-of-contents)**

173. ### What are common volume management practices?

     - **Name your volumes** for traceability (avoid anonymous ones).
     - **Back up regularly** and test restores.
     - Use **read-only mounts** (`:ro`) where the container shouldn't write.
     - **Avoid mounting sensitive host directories** directly.
     - **Prune unused volumes** periodically (`docker volume prune`).
     - **Label volumes** with metadata (owner, app, environment).
     - Document which volumes hold critical data.

     **[⬆ Back to Top](#table-of-contents)**

174. ### How do you secure Docker volumes?

     - **Mount read-only** when write access isn't needed: `-v data:/data:ro`.
     - **Set correct ownership/permissions** so non-root container users can access only what they need.
     - **Avoid exposing sensitive host paths** (e.g., never bind-mount `/` or `/etc`).
     - **Encrypt the underlying filesystem** (LUKS, fscrypt) for sensitive data at rest.
     - Use **SELinux/AppArmor** labels (e.g., `:Z`/`:z` for SELinux relabeling).

     ```bash
     docker run -v secrets:/run/secrets:ro --security-opt label=type:container_t myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

175. ### How do bind mounts impact portability?

     Bind mounts depend on a **specific host filesystem path existing**, which makes them **less portable** — the same `docker run` fails on a host lacking that path, and behavior differs across Linux, Windows, and macOS (path formats, permissions, performance). **Volumes** abstract away the host layout and are managed by Docker, so they move cleanly between environments. Prefer volumes for anything beyond local development.

     **[⬆ Back to Top](#table-of-contents)**

176. ### What are volume plugins?

     **Volume plugins (drivers)** let containers use **external storage systems** — NFS, Amazon EBS, Azure Files, GlusterFS, Ceph, Portworx, etc. They integrate third-party storage so volumes can be network-attached, replicated, or backed by cloud block storage, enabling persistence across hosts in a cluster.

     ```bash
     docker volume create -d rexray/ebs --opt size=20 myebsvol
     ```

     **[⬆ Back to Top](#table-of-contents)**

177. ### How do you migrate Docker data?

     - **Volume backups** — `tar` the volume, copy the archive, restore on the target (see Q171/Q172).
     - **`docker save`/`load`** — for moving images.
     - **Shared/network storage** — back volumes with NFS so multiple hosts access the same data.
     - **`docker cp`** or **`rsync`** — for ad-hoc file transfers.

     ```bash
     # Move a volume between hosts via a tar stream over SSH
     docker run --rm -v mydata:/data busybox tar czf - -C /data . | \
       ssh user@target 'docker run --rm -i -v mydata:/data busybox tar xzf - -C /data'
     ```

     **[⬆ Back to Top](#table-of-contents)**

178. ### How do you troubleshoot volume issues?

     ```bash
     # 1. Confirm the mount exists and where it points
     docker inspect --format '{{json .Mounts}}' mycontainer

     # 2. Check the host path and permissions
     docker volume inspect myvol
     sudo ls -la /var/lib/docker/volumes/myvol/_data

     # 3. Verify free space
     df -h /var/lib/docker

     # 4. Test write access from inside the container
     docker exec -it mycontainer touch /data/testfile
     ```

     Common issues: missing host path (bind mounts), permission mismatches (UID/GID), full disk, or SELinux denials (need `:Z`).

     **[⬆ Back to Top](#table-of-contents)**

179. ### What are storage performance considerations?

     - The **storage driver** matters — overlay2 on ext4/xfs performs well; older drivers are slower.
     - Use **dedicated, fast disks (SSD/NVMe)** for `/var/lib/docker`.
     - Avoid **slow networked storage** for high-IOPS workloads.
     - For databases, prefer **volumes over the writable layer** (CoW overhead hurts write-heavy apps).
     - Use **tmpfs** for high-speed temporary data.
     - **Monitor IOPS and latency** to spot saturation.

     **[⬆ Back to Top](#table-of-contents)**

180. ### How can volume performance be optimized?

     - Use **local SSDs/NVMe** and the **overlay2** driver.
     - Mount with **`noatime`** to skip access-time metadata writes.
     - **Minimize unnecessary I/O** in the application.
     - Use **tmpfs** for ephemeral high-throughput data.
     - For very high throughput, consider **direct LVM thin provisioning** or a **tuned network storage** backend with caching.
     - Keep frequently written data on **volumes**, not the CoW writable layer.

     **[⬆ Back to Top](#table-of-contents)**


## Docker Compose

181. ### What is Docker Compose?

     **Docker Compose** is a tool for **defining and running multi-container applications** using a declarative YAML file. Instead of typing many `docker run` commands, you describe all services, networks, and volumes in `compose.yaml` and bring the whole stack up or down with a single command.

     ```bash
     docker compose up -d      # start the entire stack
     docker compose down       # tear it down
     ```

     **[⬆ Back to Top](#table-of-contents)**

182. ### Why is Docker Compose used?

     Compose captures an **entire application stack in one declarative file**, giving you reproducible environments, one-command startup/teardown, automatic network and volume creation, and easy local development and testing. It removes the need to remember and chain long `docker run` invocations and keeps configuration in version control.

     **[⬆ Back to Top](#table-of-contents)**

183. ### What problems does Docker Compose solve?

     - **Multi-container coordination** — wiring together app, database, cache, and proxy.
     - **Networking** — auto-creates a shared network with name-based discovery.
     - **Dependency ordering** — `depends_on` controls startup order.
     - **Configuration** — centralizes env vars, ports, and volumes.
     - **Lifecycle** — `up`/`down` manage the whole stack atomically.

     **[⬆ Back to Top](#table-of-contents)**

184. ### What is a compose.yaml file?

     `compose.yaml` (formerly `docker-compose.yml`) is the YAML file describing **services, networks, volumes, secrets, and configs** for a Compose application.

     ```yaml
     services:
       web:
         image: nginx:1.27
         ports:
           - "80:80"
         depends_on:
           - app
       app:
         build: .
         environment:
           - DB_HOST=db
       db:
         image: postgres:16
         environment:
           - POSTGRES_PASSWORD=secret
         volumes:
           - dbdata:/var/lib/postgresql/data
     volumes:
       dbdata:
     ```

     (Modern Compose V2 no longer requires the top-level `version` key.)

     **[⬆ Back to Top](#table-of-contents)**

185. ### What are services in Docker Compose?

     A **service** is a definition of how to run one component of your app — which image (or build), ports, environment, volumes, networks, and replica count. Compose creates one or more containers per service. Services can be scaled to multiple replicas.

     ```bash
     docker compose up --scale app=3 -d   # run 3 instances of the 'app' service
     ```

     **[⬆ Back to Top](#table-of-contents)**

186. ### How do you define multiple containers in Compose?

     List each component under the top-level `services:` key. Each entry specifies an `image` or `build`, plus its configuration.

     ```yaml
     services:
       frontend:
         build: ./frontend
         ports: ["3000:3000"]
       backend:
         build: ./backend
         environment: [DATABASE_URL=postgres://db:5432/app]
         depends_on: [db]
       db:
         image: postgres:16
         volumes: ["dbdata:/var/lib/postgresql/data"]
       cache:
         image: redis:7
     volumes:
       dbdata:
     ```

     **[⬆ Back to Top](#table-of-contents)**

187. ### How do networks work in Docker Compose?

     Compose automatically creates a **default network** for the project, and all services join it — so they reach each other by **service name**. You can also declare **custom networks** and assign services to them for finer isolation (e.g., separating frontend and backend tiers).

     ```yaml
     services:
       web:
         networks: [frontend]
       api:
         networks: [frontend, backend]
       db:
         networks: [backend]
     networks:
       frontend:
       backend:
     ```

     **[⬆ Back to Top](#table-of-contents)**

188. ### How do volumes work in Docker Compose?

     Declare named volumes under the top-level `volumes:` key and mount them into services via each service's `volumes:` list. Compose creates and manages the volume, persisting data across `up`/`down` cycles.

     ```yaml
     services:
       db:
         image: postgres:16
         volumes:
           - dbdata:/var/lib/postgresql/data          # named volume
           - ./init.sql:/docker-entrypoint-initdb.d/init.sql:ro  # bind mount
     volumes:
       dbdata:
     ```

     **[⬆ Back to Top](#table-of-contents)**

189. ### What is depends_on?

     **`depends_on`** declares **startup/shutdown order** between services — dependencies start first and stop last. By itself it only waits for the container to *start*, not to be *ready*. With the **`condition`** form (Compose V2), you can wait for `service_started`, `service_healthy` (requires a healthcheck), or `service_completed_successfully`.

     ```yaml
     services:
       app:
         depends_on:
           db:
             condition: service_healthy   # wait until db's healthcheck passes
       db:
         image: postgres:16
         healthcheck:
           test: ["CMD-SHELL", "pg_isready -U postgres"]
           interval: 5s
           retries: 5
     ```

     **[⬆ Back to Top](#table-of-contents)**

190. ### What are environment variables in Compose?

     Set environment variables per service via the **`environment`** key or an **`env_file`**, and use **variable substitution** (`${VAR}`) pulling from your shell or a `.env` file in the project directory.

     ```yaml
     services:
       app:
         image: myapp:${APP_VERSION:-latest}   # default to 'latest' if unset
         environment:
           - DB_HOST=db
           - LOG_LEVEL=${LOG_LEVEL}
         env_file:
           - .env.production
     ```

     **[⬆ Back to Top](#table-of-contents)**

191. ### How do Compose profiles work?

     **Profiles** let you include or exclude services depending on the scenario, so one file can serve dev, test, and prod. Services without a profile always run; services tagged with a profile run only when that profile is activated.

     ```yaml
     services:
       app:
         image: myapp
       debug-tools:
         image: busybox
         profiles: [debug]
       metrics:
         image: prom/prometheus
         profiles: [monitoring]
     ```

     ```bash
     docker compose --profile debug --profile monitoring up -d
     ```

     **[⬆ Back to Top](#table-of-contents)**

192. ### How do you scale services using Compose?

     ```bash
     docker compose up -d --scale worker=5     # run 5 replicas of 'worker'
     ```

     ```yaml
     services:
       worker:
         image: myworker
         deploy:
           replicas: 5        # declarative scale (honored by 'docker stack deploy')
     ```

     Put a reverse proxy or load balancer in front to distribute traffic across replicas. Don't statically publish the same host port for a scaled service — let the proxy route.

     **[⬆ Back to Top](#table-of-contents)**

193. ### What is the difference between docker run and Compose?

     `docker run` manages a **single container** with all options crammed into one (often long) command. **Compose** orchestrates **multiple containers** with their networks, volumes, dependencies, and configuration declared in a versioned YAML file. Compose is reproducible and self-documenting; `docker run` is fine for one-offs but unwieldy for multi-service stacks.

     **[⬆ Back to Top](#table-of-contents)**

194. ### How do you start Compose services?

     ```bash
     docker compose up                 # start in foreground (logs stream)
     docker compose up -d              # detached (background)
     docker compose up --build         # rebuild images first
     docker compose up -d web db       # start only specific services
     ```

     Compose pulls missing images, builds any `build:` services, creates networks/volumes, and starts containers in dependency order.

     **[⬆ Back to Top](#table-of-contents)**

195. ### How do you stop Compose services?

     ```bash
     docker compose down               # stop and remove containers + networks
     docker compose down -v            # also remove named volumes (data loss!)
     docker compose stop               # stop containers but keep them
     docker compose down --rmi all     # also remove images
     ```

     `stop` halts without removing (resume with `start`); `down` tears down the stack. Add `-v` only when you intend to delete persisted data.

     **[⬆ Back to Top](#table-of-contents)**

196. ### How do you rebuild services in Compose?

     ```bash
     docker compose build              # rebuild all build: services
     docker compose build --no-cache   # force clean rebuild
     docker compose up -d --build      # rebuild then restart
     docker compose build api          # rebuild only one service
     ```

     Use `--no-cache` when you suspect stale cached layers are causing issues.

     **[⬆ Back to Top](#table-of-contents)**

197. ### How do you override Compose files?

     Compose **merges multiple files**, with later files taking precedence — ideal for environment-specific overrides. By default it auto-merges `compose.yaml` with `compose.override.yaml`.

     ```bash
     docker compose -f compose.yaml -f compose.prod.yaml up -d
     ```

     ```yaml
     # compose.prod.yaml — override just what differs in prod
     services:
       app:
         environment:
           - LOG_LEVEL=warn
         deploy:
           replicas: 4
     ```

     **[⬆ Back to Top](#table-of-contents)**

198. ### How do you debug Docker Compose applications?

     ```bash
     docker compose ps                       # status of all services
     docker compose logs -f                  # follow logs for all services
     docker compose logs -f api              # logs for one service
     docker compose exec api sh              # shell into a running service
     docker compose config                   # validate & view the merged config
     docker compose top                      # processes per service
     ```

     Combine `depends_on` with health checks to fix startup-order races, and use `config` to catch YAML or substitution errors before they cause failures.

     **[⬆ Back to Top](#table-of-contents)**

199. ### How do you use secrets in Compose?

     Define **secrets** and reference them in services; Compose mounts each secret as a file under **`/run/secrets/<name>`** (rather than exposing it as an env var, which is safer).

     ```yaml
     services:
       db:
         image: mysql:8
         environment:
           MYSQL_ROOT_PASSWORD_FILE: /run/secrets/db_password
         secrets:
           - db_password
     secrets:
       db_password:
         file: ./db_password.txt
     ```

     This keeps sensitive values out of the image, environment, and `docker inspect` output.

     **[⬆ Back to Top](#table-of-contents)**

200. ### How do health checks work in Compose?

     Define a **`healthcheck`** per service with a test command and timing parameters. Compose marks each container healthy/unhealthy and can gate dependents via `depends_on: condition: service_healthy`.

     ```yaml
     services:
       api:
         image: myapi
         healthcheck:
           test: ["CMD", "curl", "-f", "http://localhost:8080/health"]
           interval: 30s
           timeout: 5s
           retries: 3
           start_period: 10s
     ```

     **[⬆ Back to Top](#table-of-contents)**

201. ### How do Compose networks enable service discovery?

     Compose attaches all services to a **project network** and registers each service name in the embedded **DNS**. When one container looks up another service by name (e.g., `db`), DNS returns its current IP — no hardcoded addresses needed. Networks are namespaced by project name to isolate stacks from one another.

     ```yaml
     services:
       app:
         environment:
           - DB_HOST=db        # 'db' resolves automatically via Compose DNS
       db:
         image: postgres:16
     ```

     **[⬆ Back to Top](#table-of-contents)**

202. ### What are Compose best practices?

     - Use **descriptive service names**.
     - Externalize config with **environment variables** and **`.env`** files.
     - Use **named volumes** instead of anonymous ones.
     - Avoid **hardcoding host ports** in development; let the proxy or dynamic ports handle it.
     - Use **health checks** with `depends_on` conditions for reliable startup.
     - Separate **dev/prod** with override files or profiles.
     - Keep secrets out of the file — use **secrets** or env files (gitignored).
     - Pin **image versions** for reproducibility.

     **[⬆ Back to Top](#table-of-contents)**

203. ### How do you deploy Compose applications?

     Compose targets development and testing on a single host. For production:

     - **Docker Swarm** — `docker stack deploy -c compose.yaml mystack` runs the Compose file across a cluster.
     - **Kubernetes** — convert with **`kompose`** or rewrite as manifests/Helm charts.
     - **Single-host prod** — `docker compose up -d` with restart policies and a reverse proxy is acceptable for simple deployments.

     ```bash
     docker stack deploy -c compose.yaml myapp   # Swarm deployment
     kompose convert -f compose.yaml             # generate K8s manifests
     ```

     **[⬆ Back to Top](#table-of-contents)**

204. ### How do you monitor Compose services?

     ```bash
     docker compose ps          # service status & health
     docker compose logs -f     # aggregated logs
     docker compose top         # processes
     docker compose stats       # resource usage (via docker stats)
     ```

     For richer monitoring, add **cAdvisor + Prometheus + Grafana** as services in the Compose file, and rely on health checks to surface unhealthy containers. For production-grade observability, move to an orchestrator.

     **[⬆ Back to Top](#table-of-contents)**

205. ### What are common Compose interview scenarios?

     - Build a **multi-service app** (web + API + database + cache).
     - Inject configuration via **environment variables** and `.env`.
     - Use **build args** and **multi-stage builds** in service images.
     - Wire up **named volumes** for persistent data.
     - Define **custom networks** for tier isolation.
     - Control **startup order** with `depends_on` + health checks.
     - **Scale** a stateless service and front it with a proxy.
     - Inject **secrets** securely.
     - Provide **dev vs prod** configs via override files/profiles.

     **[⬆ Back to Top](#table-of-contents)**


## Registry & Docker Hub

206. ### What is Docker Hub?

     **Docker Hub** is the default cloud-based **container image registry**. It offers public and private repositories, official and verified-publisher images, automated builds, webhooks, organization/team management, and basic vulnerability scanning. When you `docker pull`/`docker push` without specifying a registry, Docker Hub is used by default.

     ```bash
     docker pull redis:7                    # pulls library/redis:7 from Docker Hub
     docker push myuser/myapp:1.0           # pushes to your Docker Hub repo
     ```

     **[⬆ Back to Top](#table-of-contents)**

207. ### What is a private registry?

     A **private registry** is a self-hosted or managed registry (e.g., **Harbor**, **JFrog Artifactory**, **Quay**, cloud registries) for storing images internally. It provides access control, vulnerability scanning, replication, and retention. The simplest option is running the official `registry:2` image locally.

     ```bash
     docker run -d -p 5000:5000 --restart=always --name registry registry:2
     docker tag myapp:1.0 localhost:5000/myapp:1.0
     docker push localhost:5000/myapp:1.0
     ```

     **[⬆ Back to Top](#table-of-contents)**

208. ### How do you push images to Docker Hub?

     ```bash
     # 1. Log in
     docker login
     # 2. Tag with your namespace
     docker tag myapp:1.0 myuser/myapp:1.0
     # 3. Push
     docker push myuser/myapp:1.0
     ```

     The image (and its layers not already present) uploads to your repository. Use descriptive, versioned tags rather than `latest` for production.

     **[⬆ Back to Top](#table-of-contents)**

209. ### How do you pull images from Docker Hub?

     ```bash
     docker pull myuser/myapp:1.0           # specific user repo + tag
     docker pull nginx                       # library/nginx:latest (official image)
     docker pull nginx@sha256:abcd...        # pull an exact digest
     ```

     If you omit the username, Docker assumes the official `library` namespace; if you omit the tag, it defaults to `latest`.

     **[⬆ Back to Top](#table-of-contents)**

210. ### What is image versioning strategy?

     A good strategy combines multiple tagging schemes for traceability:

     - **Semantic versioning** — `1.2.3`, plus moving tags `1.2` and `1`.
     - **Environment tags** — `dev`, `staging`, `prod`.
     - **Git commit SHA** — `app:a1b2c3d` ties an image to exact source.
     - **Build numbers** — `app:build-456` for CI traceability.

     Avoid `latest` in production. Combining a semantic version with an immutable commit SHA gives both readability and precise traceability.

     **[⬆ Back to Top](#table-of-contents)**

211. ### How do you authenticate with a Docker registry?

     ```bash
     docker login                            # Docker Hub
     docker login registry.example.com       # private registry
     docker login -u myuser --password-stdin < token.txt   # token-based
     ```

     Credentials are stored in `~/.docker/config.json` or, more securely, via **credential helpers** (`docker-credential-helpers`) that integrate with the OS keychain or cloud IAM.

     **[⬆ Back to Top](#table-of-contents)**

212. ### What are Docker Hub organizations?

     **Organizations** let groups manage repositories, teams, and permissions collectively. You create teams with **read**, **write**, or **admin** access to specific repositories, enabling company-wide image governance and controlled collaboration across many developers.

     **[⬆ Back to Top](#table-of-contents)**

213. ### How do you host a private registry?

     Run the official registry image, then secure it with TLS and authentication:

     ```bash
     # Basic local registry
     docker run -d -p 5000:5000 --restart=always --name registry \
       -v registry-data:/var/lib/registry registry:2

     # With TLS and basic auth
     docker run -d -p 443:5000 --restart=always --name registry \
       -v "$(pwd)"/certs:/certs \
       -v "$(pwd)"/auth:/auth \
       -e REGISTRY_HTTP_TLS_CERTIFICATE=/certs/domain.crt \
       -e REGISTRY_HTTP_TLS_KEY=/certs/domain.key \
       -e "REGISTRY_AUTH=htpasswd" \
       -e "REGISTRY_AUTH_HTPASSWD_REALM=Registry" \
       -e REGISTRY_AUTH_HTPASSWD_PATH=/auth/htpasswd \
       registry:2
     ```

     For enterprise features (RBAC, scanning, replication), use **Harbor** or **Artifactory**.

     **[⬆ Back to Top](#table-of-contents)**

214. ### What is Harbor?

     **Harbor** is an open-source, enterprise-grade registry (a CNCF graduated project) that extends the basic Docker registry with **role-based access control (RBAC)**, **image replication** across registries, **vulnerability scanning** (Trivy), **content signing** (Notary/Cosign), LDAP/SSO integration, and retention/quota policies. It's a popular self-hosted alternative to cloud registries.

     **[⬆ Back to Top](#table-of-contents)**

215. ### What is Amazon ECR?

     **Amazon Elastic Container Registry (ECR)** is AWS's managed registry. It integrates with **IAM** for authentication/authorization, offers image **scanning**, **lifecycle policies**, and **cross-region/cross-account replication**, and works seamlessly with ECS, EKS, and Lambda.

     ```bash
     aws ecr get-login-password --region us-east-1 | \
       docker login --username AWS --password-stdin \
       123456789.dkr.ecr.us-east-1.amazonaws.com
     docker push 123456789.dkr.ecr.us-east-1.amazonaws.com/myapp:1.0
     ```

     **[⬆ Back to Top](#table-of-contents)**

216. ### What is Azure Container Registry (ACR)?

     **Azure Container Registry (ACR)** is Azure's managed registry. It supports **geo-replication**, vulnerability scanning via **Microsoft Defender**, integration with **Azure Active Directory**, and ACR Tasks for cloud-based image builds. Manage it with the `az acr` CLI.

     ```bash
     az acr login --name myregistry
     docker push myregistry.azurecr.io/myapp:1.0
     ```

     **[⬆ Back to Top](#table-of-contents)**

217. ### What is Google Artifact Registry?

     **Google Artifact Registry** (the successor to Container Registry) is GCP's managed registry for container images and other artifacts. It supports **multi-region replication**, integrated **IAM**, and **vulnerability scanning**, and integrates with GKE and Cloud Build. Manage it with `gcloud artifacts`.

     ```bash
     gcloud auth configure-docker us-central1-docker.pkg.dev
     docker push us-central1-docker.pkg.dev/my-project/my-repo/myapp:1.0
     ```

     **[⬆ Back to Top](#table-of-contents)**

218. ### How do you secure container registries?

     - **Require TLS** for all registry communication.
     - **Enforce authentication and authorization** (RBAC, IAM).
     - **Enable vulnerability scanning** and block vulnerable images.
     - **Sign images** (Docker Content Trust / Cosign) and verify on pull.
     - **Replicate** images for availability and disaster recovery.
     - Define **retention policies** to prune old/unused tags.
     - **Monitor access logs** and audit pushes/pulls.

     **[⬆ Back to Top](#table-of-contents)**

219. ### How do you replicate images across registries?

     Use built-in registry features or copy tools:

     ```bash
     # skopeo — copy directly between registries without a local pull
     skopeo copy docker://src-registry/myapp:1.0 docker://dst-registry/myapp:1.0

     # crane — similar lightweight copy
     crane copy src-registry/myapp:1.0 dst-registry/myapp:1.0
     ```

     **Harbor** offers scheduled replication rules; **ECR/ACR/GAR** provide native cross-region replication. Replication improves availability, reduces pull latency, and supports DR.

     **[⬆ Back to Top](#table-of-contents)**

220. ### What are image retention policies?

     **Retention policies** automatically delete old or surplus image tags based on criteria like **age**, **number of versions to keep**, or **untagged status**. They control storage growth, reduce costs, and enforce lifecycle hygiene. Configure them per repository in Harbor, ECR (lifecycle policies), ACR, or Artifact Registry.

     ```json
     // Example ECR lifecycle policy: keep only the 10 most recent images
     {
       "rules": [{
         "rulePriority": 1,
         "selection": { "tagStatus": "any", "countType": "imageCountMoreThan", "countNumber": 10 },
         "action": { "type": "expire" }
       }]
     }
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Docker Security

221. ### What are major security risks in Docker?

     | Risk | Why it's dangerous |
     | --- | --- |
     | **Running as root** | Container escape gains host root |
     | **Untrusted images** | May contain malware or backdoors |
     | **Exposed ports** | Increases attack surface |
     | **Misconfigured host mounts** | Container can read/write sensitive host files |
     | **`--privileged` / host networking** | Removes isolation boundaries |
     | **Outdated base images** | Unpatched CVEs |
     | **Secrets in images/env** | Credentials leak via layers or `inspect` |

     **[⬆ Back to Top](#table-of-contents)**

222. ### How does container isolation improve security?

     Isolation layers reduce the blast radius of a compromise:

     - **Namespaces** isolate processes, network, mounts, and IPC so a container can't see or touch others.
     - **cgroups** prevent resource exhaustion (DoS) of the host.
     - **Capabilities** restrict which privileged operations are allowed.
     - **seccomp** filters dangerous syscalls.
     - **AppArmor/SELinux** add mandatory access control.

     Together they confine a container so that even a compromised process has limited reach.

     **[⬆ Back to Top](#table-of-contents)**

223. ### Why should containers not run as root?

     If a process runs as **root inside the container** and an attacker exploits it, a container escape (via a kernel or misconfiguration bug) can yield **root on the host**. Running as a **non-privileged user** with `USER` drops that risk dramatically — an escape lands as an unprivileged user. Dropping unnecessary capabilities further hardens the container.

     **[⬆ Back to Top](#table-of-contents)**

224. ### How do you run containers as non-root users?

     Create a user in the Dockerfile and switch to it with `USER`, or pass `--user` at run time:

     ```dockerfile
     FROM python:3.12-slim
     RUN adduser --disabled-password --gecos '' appuser
     USER appuser
     WORKDIR /app
     COPY --chown=appuser:appuser . .
     CMD ["python", "app.py"]
     ```

     ```bash
     docker run --user 1000:1000 myapp     # override UID:GID at runtime
     ```

     **[⬆ Back to Top](#table-of-contents)**

225. ### What are Linux capabilities in Docker?

     **Capabilities** split root's monolithic privileges into discrete units (e.g., `CAP_NET_ADMIN`, `CAP_SYS_ADMIN`, `CAP_NET_BIND_SERVICE`). Docker **drops most capabilities by default** and lets you fine-tune with `--cap-add` and `--cap-drop`. Best practice is to **drop all and add back only what's needed**.

     ```bash
     docker run --cap-drop=ALL --cap-add=NET_BIND_SERVICE nginx
     ```

     **[⬆ Back to Top](#table-of-contents)**

226. ### How do seccomp profiles work?

     **seccomp (secure computing mode)** filters the **system calls** a container may make. Docker applies a **default seccomp profile** that blocks dangerous syscalls (e.g., loading kernel modules, mounting filesystems) while allowing common ones. You can supply a custom profile to tighten or loosen the allowlist.

     ```bash
     docker run --security-opt seccomp=/path/to/profile.json myapp
     docker run --security-opt seccomp=unconfined myapp   # disable (NOT recommended)
     ```

     **[⬆ Back to Top](#table-of-contents)**

227. ### What is AppArmor in Docker?

     **AppArmor** is a Linux Security Module that confines programs to a defined set of capabilities and file access via a **profile**. Docker ships a **default AppArmor profile** (`docker-default`) for containers; you can apply a custom one for stricter mandatory access control.

     ```bash
     docker run --security-opt apparmor=my-custom-profile myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

228. ### What is SELinux integration in Docker?

     **SELinux** labels processes and files and enforces mandatory access control based on those labels. With SELinux enabled, Docker confines container processes so they **cannot access host files** unless properly labeled. For shared volumes, append **`:z`** (shared) or **`:Z`** (private) to relabel them for container access.

     ```bash
     docker run -v /host/data:/data:Z myapp   # relabel volume for this container
     ```

     **[⬆ Back to Top](#table-of-contents)**

229. ### How do Docker secrets work?

     **Secrets** securely deliver sensitive data (passwords, tokens, keys) to containers as **files mounted at `/run/secrets/<name>`**, rather than as environment variables or baked into images. In **Swarm** (and Kubernetes), secrets are **encrypted at rest and in transit** and only delivered to services that need them.

     ```bash
     echo "s3cr3t" | docker secret create db_password -
     docker service create --name db --secret db_password mysql:8
     # Inside the container: cat /run/secrets/db_password
     ```

     **[⬆ Back to Top](#table-of-contents)**

230. ### How do you secure sensitive environment variables?

     - **Avoid putting secrets in env vars or image layers** — they leak via `docker inspect`, logs, and image history.
     - Use **Docker/Swarm secrets** or **Kubernetes Secrets** (file-mounted).
     - Integrate a **secrets manager** (HashiCorp Vault, AWS Secrets Manager).
     - If env vars are unavoidable, ensure they're **never logged** and inject them at runtime, not build time.
     - Use **build secrets** (`RUN --mount=type=secret`) so they don't persist in layers.

     ```dockerfile
     # syntax=docker/dockerfile:1
     RUN --mount=type=secret,id=npmtoken \
         NPM_TOKEN=$(cat /run/secrets/npmtoken) npm install
     ```

     **[⬆ Back to Top](#table-of-contents)**

231. ### How do you scan Docker images for vulnerabilities?

     ```bash
     docker scout cves myapp:1.0          # Docker's built-in scanner
     trivy image myapp:1.0                # open-source, fast, popular
     grype myapp:1.0                      # Anchore's scanner
     ```

     Best practices: **scan in CI** and fail builds on critical CVEs, **regularly rebuild** on patched base images, use **multi-stage builds** to strip build tools, and prefer **minimal base images** to shrink the attack surface.

     **[⬆ Back to Top](#table-of-contents)**

232. ### What is Docker Content Trust?

     **Docker Content Trust (DCT)** uses **Notary** to **digitally sign and verify** image tags. With `DOCKER_CONTENT_TRUST=1`, Docker only pulls/runs images whose signatures are valid, guaranteeing **integrity and publisher authenticity** and preventing tampered or man-in-the-middle images.

     ```bash
     export DOCKER_CONTENT_TRUST=1
     docker push myuser/myapp:1.0     # signs the image
     docker pull myuser/myapp:1.0     # verifies the signature before running
     ```

     (Cosign/Sigstore is the modern, widely adopted alternative for signing.)

     **[⬆ Back to Top](#table-of-contents)**

233. ### How does image signing work?

     Publishers **sign image metadata** (tag → digest mappings) with a **private key** via Notary or Cosign; the corresponding **public key** lets consumers verify the signature before pulling. If the signature is missing or invalid, the pull is rejected. This ensures the image you run is exactly what the trusted publisher produced — preventing tampering and supply-chain attacks.

     **[⬆ Back to Top](#table-of-contents)**

234. ### How do you harden Docker containers?

     - Use **minimal base images** (Alpine, distroless).
     - **Remove package managers and compilers** from the final image.
     - **Run as non-root** (`USER`) and use `--read-only` root filesystem where possible.
     - **Drop all capabilities**, add back only what's needed; avoid `--privileged`.
     - Apply **seccomp, AppArmor/SELinux** profiles.
     - **Limit resources** with cgroups; set `--pids-limit`.
     - **Keep images patched**; scan regularly.
     - Avoid **host networking** and untrusted bind mounts.
     - Set **`--security-opt no-new-privileges`**.

     ```bash
     docker run --read-only --cap-drop=ALL --security-opt no-new-privileges \
       --pids-limit=100 --memory=256m myapp
     ```

     **[⬆ Back to Top](#table-of-contents)**

235. ### What are Docker security best practices?

     - **Don't run SSH** inside containers (use `docker exec`).
     - Avoid **`--privileged`** and **`--net=host`** unless absolutely required.
     - Use **official or trusted-source images**; verify signatures.
     - Run as **non-root** and **drop capabilities**.
     - Enable **AppArmor/SELinux** and **seccomp** profiles.
     - Keep the **host OS and Docker patched**.
     - Use **secrets management**, never bake secrets into images.
     - **Limit resources** and apply **network policies**.
     - Use **rootless mode**, which runs the daemon and containers in an unprivileged user namespace, sharply reducing the risk of root-level exploits.

     **[⬆ Back to Top](#table-of-contents)**


## Docker Swarm & Orchestration

236. ### What is Docker Swarm?

     **Docker Swarm** is Docker's built-in **container orchestrator**. It turns a pool of Docker hosts into a single virtual host (a "swarm"), letting you deploy and manage **services** across many machines. Swarm handles **scheduling, service discovery, load balancing, scaling, and rolling updates** natively — no extra tooling required.

     ```bash
     docker swarm init                                     # create a swarm
     docker service create --replicas 3 -p 80:80 nginx     # deploy a service
     ```

     **[⬆ Back to Top](#table-of-contents)**

237. ### How does Docker Swarm work?

     A swarm consists of **manager nodes** and **worker nodes**. Managers maintain cluster state, schedule tasks, and **elect a leader** using the **Raft consensus** algorithm (which replicates state for fault tolerance). Workers run the tasks (containers) assigned by managers. The desired state (e.g., "3 replicas of web") is continuously reconciled against the actual state.

     **[⬆ Back to Top](#table-of-contents)**

238. ### What is a Swarm manager node?

     A **manager node** stores the cluster state, manages node membership, schedules services, and exposes the Swarm API. Managers participate in **Raft-based leader election** and replicate state among themselves. For high availability, run an **odd number** of managers (3 or 5) so a majority quorum can survive failures — 3 managers tolerate 1 failure, 5 tolerate 2.

     **[⬆ Back to Top](#table-of-contents)**

239. ### What is a Swarm worker node?

     A **worker node** runs the **tasks (containers)** assigned by managers but does **not** participate in Raft consensus or scheduling decisions. If a worker fails, its tasks are **rescheduled** onto healthy nodes to maintain the desired state. Workers can be promoted to managers (and vice versa) as needed.

     ```bash
     docker node promote worker1     # promote a worker to manager
     docker node ls                  # view all nodes and roles
     ```

     **[⬆ Back to Top](#table-of-contents)**

240. ### How do you initialize a Swarm cluster?

     ```bash
     # On the first manager
     docker swarm init --advertise-addr 192.168.1.10
     # Outputs a join command/token for workers

     # On each worker
     docker swarm join --token SWMTKN-1-xxxx 192.168.1.10:2377

     # Get the manager join token to add more managers
     docker swarm join-token manager
     ```

     Port **2377** is used for cluster management traffic. After joining, `docker node ls` (on a manager) shows the cluster.

     **[⬆ Back to Top](#table-of-contents)**

241. ### What are Docker services?

     A **service** is the Swarm-level definition of a workload: the image, command, ports, networks, constraints, and **replica count**. Swarm ensures the specified number of **tasks** (container instances) are always running, rescheduling them on failure.

     ```bash
     docker service create --name web --replicas 3 -p 80:80 nginx
     docker service ls
     docker service ps web        # see individual tasks and their nodes
     ```

     **[⬆ Back to Top](#table-of-contents)**

242. ### What is desired state management in Swarm?

     Swarm stores the **desired state** of each service (replica count, networks, constraints) and continuously **reconciles** the actual cluster state toward it. If a container crashes or a node dies, managers automatically **schedule replacement tasks** to restore the declared count — self-healing without manual intervention.

     ```bash
     docker service create --name api --replicas 5 myapi
     # Kill a container or node → Swarm starts a replacement to keep 5 running
     ```

     **[⬆ Back to Top](#table-of-contents)**

243. ### How does service scaling work in Swarm?

     ```bash
     docker service scale web=10        # change replica count
     docker service update --replicas 10 web   # equivalent
     ```

     Swarm schedules additional tasks (or removes excess) to reach the target count, **balancing them across available nodes** according to scheduling constraints and resource availability. The routing mesh load-balances incoming traffic across all replicas.

     **[⬆ Back to Top](#table-of-contents)**

244. ### What is a rolling update in Swarm?

     A **rolling update** replaces service tasks **incrementally** rather than all at once, minimizing downtime. Swarm stops a batch, starts new tasks with the updated image, waits for health, then proceeds to the next batch. You control **parallelism**, **delay**, and **failure action**. If an update fails, **`docker service rollback`** reverts to the previous version.

     ```bash
     docker service update \
       --image myapp:2.0 \
       --update-parallelism 2 \
       --update-delay 10s \
       --update-failure-action rollback \
       web
     ```

     **[⬆ Back to Top](#table-of-contents)**

245. ### What is service rollback in Swarm?

     **`docker service rollback`** reverts a service to its **previous specification** after a failed or problematic update. Swarm terminates the new tasks and redeploys the prior version, using the same incremental, low-downtime mechanism as updates. Configuring `--update-failure-action rollback` makes this automatic when an update's health checks fail.

     ```bash
     docker service rollback web
     ```

     Pair rollbacks with health checks and monitoring/alerts to detect bad deployments early.

     **[⬆ Back to Top](#table-of-contents)**


## Advanced & Scenario-Based Questions

246. ### How would you containerize a Spring Boot microservice for production?

     Use a **multi-stage build** to compile with Maven, then ship only the JAR on a slim JRE, running as a non-root user with a health check.

     ```dockerfile
     # Stage 1: build
     FROM eclipse-temurin:17-jdk-alpine AS build
     WORKDIR /app
     COPY mvnw .
     COPY .mvn .mvn
     COPY pom.xml .
     RUN ./mvnw dependency:go-offline        # cache dependencies
     COPY src src
     RUN ./mvnw package -DskipTests

     # Stage 2: runtime
     FROM eclipse-temurin:17-jre-alpine
     RUN addgroup -S app && adduser -S -G app appuser
     WORKDIR /app
     COPY --from=build /app/target/myservice-0.0.1-SNAPSHOT.jar app.jar
     USER appuser
     EXPOSE 8080
     HEALTHCHECK --interval=30s --timeout=3s --retries=3 \
       CMD wget -qO- http://localhost:8080/actuator/health || exit 1
     ENTRYPOINT ["java","-XX:MaxRAMPercentage=75.0","-jar","/app/app.jar"]
     ```

     **Production checklist:**
     1. **Multi-stage build** keeps the toolchain out of the final image.
     2. **Run as non-root** (`appuser`).
     3. **Health check** for orchestrator readiness.
     4. **Externalize config** via env vars or a config server (`SPRING_DATASOURCE_URL`, etc.).
     5. **JVM container-awareness** (`-XX:MaxRAMPercentage`, `-XX:+UseContainerSupport`).
     6. **Persist** logs/data with volumes if needed.
     7. **Deploy** on Swarm/Kubernetes with secrets for DB credentials and service discovery.

     **[⬆ Back to Top](#table-of-contents)**

247. ### How would you reduce a 1 GB Docker image to under 200 MB?

     A layered approach, in order of impact:

     1. **Switch to a minimal base** — `alpine` or `distroless` instead of full `ubuntu`.
     2. **Use multi-stage builds** — keep only the compiled artifact in the final stage.
     3. **Remove build dependencies and caches** in the same layer.
     4. **Combine `RUN` commands** and clean package caches (`rm -rf /var/lib/apt/lists/*`).
     5. **Use `COPY` not `ADD`** and copy only what's needed.
     6. **Add `.dockerignore`** to exclude source, tests, `.git`, `node_modules`.

     ```dockerfile
     # Before: ~1 GB (full JDK + Maven + source in final image)
     # After: multi-stage → only JRE + JAR
     FROM maven:3.9-eclipse-temurin-17 AS build
     WORKDIR /app
     COPY . .
     RUN mvn package -DskipTests

     FROM eclipse-temurin:17-jre-alpine        # ~180 MB total
     COPY --from=build /app/target/app.jar /app.jar
     ENTRYPOINT ["java","-jar","/app.jar"]
     ```

     Verify with `docker images` and analyze waste with `dive`.

     **[⬆ Back to Top](#table-of-contents)**

248. ### How would you troubleshoot a container that repeatedly restarts in production?

     ```bash
     # 1. Check state and restart count
     docker inspect --format '{{.RestartCount}} {{.State.Status}} {{.State.ExitCode}}' web

     # 2. Read the last logs before each crash
     docker logs --tail 50 -f web

     # 3. Look at lifecycle events
     docker events --filter container=web

     # 4. Check for OOM kills
     docker inspect --format '{{.State.OOMKilled}}' web
     dmesg | grep -i oom
     ```

     **Systematic checklist:**
     - **Exit code clues** — `137` = OOM/SIGKILL, `139` = segfault, `1` = app error.
     - **Failing health check** can trigger restart loops — review the probe.
     - **Resource limits** too low → OOM kills; raise `--memory` or fix leaks.
     - **Missing dependencies** — DB/cache not reachable at startup.
     - **Bad config/env** — verify required variables and secrets.
     - **Reproduce locally** — `docker run -it --entrypoint sh myimage` to inspect.
     - Under an orchestrator, review the **service definition and update strategy**.

     **[⬆ Back to Top](#table-of-contents)**

249. ### How would you design a highly available Docker-based microservices platform?

     A resilient, multi-layer design:

     - **Orchestration** — Kubernetes or Docker Swarm across multiple nodes; at least **3 manager nodes** for quorum, spread across availability zones.
     - **Networking** — overlay networks for inter-service comms; ingress controllers or load balancers for external traffic.
     - **Storage** — persistent volumes on network/cloud storage (EBS, NFS, Ceph) with appropriate volume drivers.
     - **Service discovery & LB** — built-in DNS/VIP (Swarm) or Services + Ingress (K8s).
     - **Scaling** — horizontal autoscaling based on CPU/memory/custom metrics.
     - **Monitoring & logging** — Prometheus + Grafana, centralized logging (ELK/Loki), distributed tracing (Jaeger).
     - **CI/CD** — automated build/test/deploy with **blue-green or canary** rollouts.
     - **Security** — secrets management, non-root containers, image signing, scanning, network policies, rootless mode.
     - **Disaster recovery** — volume and registry backups; replicated registries (Harbor).
     - **Self-healing** — readiness/liveness probes and desired-state reconciliation.

     **[⬆ Back to Top](#table-of-contents)**

250. ### How would you optimize Docker containers running on Kubernetes for performance and cost?

     - **Resource requests/limits** — rightsize CPU and memory per pod to prevent over-provisioning and ensure fair scheduling.
     - **Slim images + multi-stage builds** — smaller images mean faster pulls, quicker cold starts, and lower storage cost.
     - **Readiness/liveness probes** — health-gate traffic and restarts instead of crash loops.
     - **initContainers** — handle one-time setup (migrations, asset prep) cleanly.
     - **Horizontal Pod Autoscaler** — scale on CPU/memory/custom metrics; add **Cluster Autoscaler** for node elasticity.
     - **JVM/runtime tuning** — container-aware flags (`-XX:MaxRAMPercentage`, `-XX:+UseContainerSupport`).
     - **Avoid `--privileged` and host networking** unless required.
     - **Node affinity, taints/tolerations** — schedule workloads on appropriate (e.g., spot) nodes for cost savings.
     - **Image pull caching** and private registries on/near nodes for faster pulls.
     - **Consolidate microservices / use sidecars judiciously** to reduce per-pod overhead.

     ```yaml
     resources:
       requests: { cpu: "250m", memory: "256Mi" }
       limits:   { cpu: "500m", memory: "512Mi" }
     ```

     **[⬆ Back to Top](#table-of-contents)**

---

### Disclaimer

The questions and answers in this repository are a curated summary of commonly asked Docker interview questions. They cover concepts from foundational through advanced and scenario-based depth, including architecture, images, containers, Dockerfiles, networking, storage, Compose, registries, security, Swarm, and real-world design. There is no guarantee that these exact questions will appear in any given interview — the purpose is to help you rapidly review key concepts and build deep understanding. Contributions and corrections are welcome.

Good luck with your interview 😊

---
