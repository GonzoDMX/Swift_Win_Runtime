FROM swift:5.9-jammy

# Installing essential packages
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    gnupg \
    libcurl4-openssl-dev \
    libxml2-dev \
    libedit-dev \
    python3 \
    python3-pip \
    sqlite3 \
    libsqlite3-dev \
    libssl-dev \
    zlib1g-dev \
    unzip \
    zip \
    man-db \
    && rm -rf /var/lib/apt/lists/*

# Install Node.js (useful for web dev students)
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs \
    && npm install -g npm@latest

# Create a non-root user
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get update \
    && apt-get install -y sudo \
    && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Install Swift-specific tools
RUN pip3 install --upgrade pip \
    && pip3 install pygments sourcekitten

# Set up Sourcekit-LSP for code navigation
RUN ln -s /usr/bin/sourcekit-lsp /usr/local/bin/sourcekit-lsp

# Setup LLDB for debugging
RUN apt-get update && apt-get install -y lldb python3-lldb-14 \
    && ln -s /usr/lib/llvm-14/lib/python3.10/dist-packages/lldb/* /usr/lib/python3/dist-packages/lldb/ \
    && rm -rf /var/lib/apt/lists/*

# Set up a working directory
WORKDIR /workspace

# Add useful shell aliases
RUN echo 'alias ll="ls -la"' >> /home/$USERNAME/.bashrc \
    && echo 'alias swiftb="swift build"' >> /home/$USERNAME/.bashrc \
    && echo 'alias swiftr="swift run"' >> /home/$USERNAME/.bashrc \
    && echo 'alias swiftt="swift test"' >> /home/$USERNAME/.bashrc

# Give ownership to the non-root user
RUN chown -R $USERNAME:$USERNAME /workspace

# Switch to the non-root user
USER $USERNAME

# Verify Swift installation
RUN swift --version

# Set default shell
ENV SHELL /bin/bash

CMD ["/bin/bash"]
