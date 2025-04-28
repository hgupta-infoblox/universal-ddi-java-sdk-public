# Universal DDI Java SDK (Public Version)

Welcome to the **Universal DDI Java SDK Public Repository**! 🚀

This SDK provides Java-based programmatic access to Infoblox Universal DDI services, such as:
- IP Address Management (IPAM)
- DNS Management
- DHCP Management

It is designed to interact with the DDI APIs in a standardized, efficient way.

---

## 📂 Repository Structure

```
/                   # Root project folder
├── sdk/             # All auto-generated SDK modules per API spec (e.g., ddi-ipam, ddi-dns, etc.)
├── sdk-core/        # Core library (Authentication, HTTP client handling, common utils)
├── pom.xml          # Root Maven project (parent POM)
├── README.md        # You are here! Project information and instructions
├── .gitignore       # Git ignore rules
└── LICENSE          # Open source license (e.g., Apache 2.0)
```

---

## 🔥 Key Highlights

- **Auto-Generated SDKs**: SDKs are generated using [OpenAPI Generator](https://openapi-generator.tech/) based on internal API specifications.
- **Modular Design**: Each major API (e.g., IPAM, DNS) is split into separate SDK modules under `sdk/`.
- **Shared Core**: `sdk-core/` contains shared functionality (e.g., authentication, token management, HTTP client setup).
- **Maven Multi-Module Project**: Easily build everything using a single Maven command.


---

## ⚙️ Building the SDK

This project uses **Maven** for building.

To build all SDK modules:

```bash
mvn clean install
```

The command will:
- Build the `sdk-core` first.
- Then build each SDK module under `sdk/`.

---

## 📦 Using the SDKs

You can consume each SDK module as a Maven dependency if you install them locally or publish them to your Maven repository.

Example (Maven dependency):

```xml
<dependency>
  <groupId>com.infoblox.universalddi</groupId>
  <artifactId>ddi-ipam</artifactId>
  <version>1.0.0</version>
</dependency>
```

(Replace `ddi-ipam` with the correct module you need.)


---

## 🛠️ SDK Generation Information

These SDKs were generated using [OpenAPI Generator](https://openapi-generator.tech/) based on internal, private Infoblox OpenAPI specifications.

> **Note:** The OpenAPI specification files (.json/.yaml) used for SDK generation are private and are not included in this public repository.

If you ever need to regenerate SDKs, you would typically run an OpenAPI Generator command like:

```bash
openapi-generator generate \
  -i [your-api-spec.json] \
  -g java \
  -o [output-directory] \
  -p useRuntimeException=true
```

---

## 📋 Contributing

Currently, direct contributions to this public SDK are restricted.

For suggestions, feature requests, or issues:
- Please open a GitHub Issue.
- Or contact the maintainers via the Infoblox support channels.


---

## 🛡️ License

This project is licensed under the [Apache 2.0 License](LICENSE).

---

## 👀 Notes for Maintainers

- **OpenAPI Specs are private** — not pushed here.
- **SDKs are generated, not manually written** — remember this when updating APIs.
- **Do not manually edit generated code** unless absolutely necessary (in that case document the change).

---

> **Maintained by:** Infoblox Engineering Team ✨

