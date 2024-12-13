# Step 2: Requirements for Apache Gora Installation

To successfully install and run Apache Gora, ensure your system meets the following requirements.

---

## Step 2.1: Install Java Development Kit (JDK)

Apache Gora requires Java 8 or later. Installing OpenJDK is recommended.

1. **Update the Package List**:

   ```bash
   sudo apt update
   ```
2. **Install OpenJDK**:

   ```bash
   sudo apt install -y openjdk-11-jdk
   ```
3. **Verify Installation**:

   ```bash
   java -version
   ```

   Expected output:

   ```
   openjdk version "11.0.x"...
   ```

---

## Step 2.2: Install Apache Maven

Apache Maven is required to build Apache Gora from source.

1. **Install Maven**:

   ```bash
   sudo apt install -y maven
   ```
2. **Verify Installation**:

   ```bash
   mvn -version
   ```

   Expected output:

   ```
   Apache Maven x.x.x...
   ```

---

## Step 2.3: Install Git

Git is needed to clone the Apache Gora repository.

1. **Install Git**:

   ```bash
   sudo apt install -y git
   ```
2. **Verify Installation**:

   ```bash
   git --version
   ```

---

## Step 2.4: Install Essential Build Tools

Additional tools are required for compiling and building the project.

1. **Install Build Tools**:

   ```bash
   sudo apt install -y build-essential
   ```
2. **Verify Installation**:

   ```bash
   gcc --version
   ```

---

## Step 2.5: Install Additional Utilities (Optional)

Optional tools can improve productivity during development.

1. **Install Utilities**:

   ```bash
   sudo apt install -y curl wget unzip
   ```
2. **Verify Installation**:

   - Test commands like `curl --version` or `wget --version` to confirm installation.

---

With all requirements installed, you are ready to proceed to [Step 3: Installing Apache Gora](step3.md).
