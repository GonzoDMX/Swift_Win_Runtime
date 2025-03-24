FROM swift:5.9-jammy

# Skip updating package lists since we're having DNS issues
RUN mkdir -p /workspace

# Create a non-root user (without installing sudo)
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

# Set up a working directory
WORKDIR /workspace
RUN chown -R $USERNAME:$USERNAME /workspace

# Switch to the non-root user
USER $USERNAME

# Verify Swift installation
RUN swift --version

# Set default shell
ENV SHELL /bin/bash
