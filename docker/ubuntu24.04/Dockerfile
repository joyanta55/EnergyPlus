FROM ubuntu:24.04

# Install system dependencies
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
    build-essential \
    g++ \
    cmake \
    cmake-curses-gui \
    git \
    python3 \
    python3-pip \
    wget \
    unzip \
    libboost-all-dev \
    libopenmpi-dev \
    gfortran \
    && apt-get clean

# Set working directory
WORKDIR /workdir

# Clone the EnergyPlus repository
RUN git clone https://github.com/NREL/EnergyPlus.git


# Run cmake
RUN cmake EnergyPlus

# Compile with 4 cores (adjust -j4 based on your needs)
RUN make -j4

RUN chmod 755 /workdir/Products/energyplus

ENTRYPOINT ["/workdir/Products/energyplus"]