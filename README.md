# Firely-net-sdk-develop

**Official .NET SDK for HL7 FHIR** – A comprehensive toolkit for working with healthcare data standards on the Microsoft .NET platform.

## 🏥 Overview
This SDK provides complete support for FHIR (Fast Healthcare Interoperability Resources) standards, enabling seamless integration of healthcare data in .NET applications.

## 📦 Core Features
- **POCO Models** – Strongly-typed classes for all FHIR resources
- **Serialization** – XML and JSON parsers/serializers
- **REST Client** – FHIR-compliant server communication
- **Validation** – Profile-based instance validation
- **FhirPath** – Expression evaluation engine
- **Metadata Tools** – StructureDefinition and differential generation

## 🚀 Getting Started
HL7 has published several FHIR specification versions with breaking changes. Choose the right version for your needs:

| Spec Version | Release Date | Status | NuGet Package |
|--------------|--------------|---------|---------------|
| **R5** | March 26, 2023 | Latest official | `Hl7.Fhir.R5` |
| **R4B** | May 2022 | Active use | `Hl7.Fhir.R4B` |
| **R4** | January 2019 | Widely deployed | `Hl7.Fhir.R4` |
| **STU3** | March 2017 | Legacy support | `Hl7.Fhir.STU3` |

**Quick start:** Most developers can begin by installing the appropriate NuGet package for their FHIR version.

## 📥 Installation
```xml
<PackageReference Include="Hl7.Fhir.R5" Version="6.0.0" />
<!-- OR -->
<PackageReference Include="Hl7.Fhir.R4" Version="6.0.0" />
```

### Pre-release Packages
Access development builds via GitHub Packages:
```bash
dotnet nuget add source --name github --username <USERNAME> \
  --password <PAT> https://nuget.pkg.github.com/FirelyTeam/index.json
```
*Requires GitHub Personal Access Token with `read:packages` scope*

## 🔄 Upgrading
We maintain compile compatibility between minor releases. Major version upgrades may include breaking changes:

| SDK Version | Breaking Changes |
|-------------|-----------------|
| 6.x | [Breaking changes in 6.0](https://github.com/FirelyTeam/firely-net-sdk/wiki/Breaking-changes-in-6.0) |
| 5.x | [Breaking changes in 5.0](https://github.com/FirelyTeam/firely-net-sdk/wiki/Breaking-changes-in-5.0) |
| 4.x | [Breaking changes in 4.0](https://github.com/FirelyTeam/firely-net-sdk/wiki/Breaking-changes-in-4.0) |

**Note:** The profile validator is now a separate package available on NuGet.

## 🛠️ Development
### Branch Strategy
- **`develop`** – Main development branch (contains STU3 through R5)
- **`release/*`** – Version-specific releases
- **`feature/*`** – New feature development

### Building
```bash
# Clone the repository
git clone https://github.com/FirelyTeam/firely-net-sdk.git
cd firely-net-sdk

# Restore dependencies
dotnet restore

# Build the solution
dotnet build
```

### Binary Compatibility
Ensure binary compatibility checks pass:
```bash
dotnet pack /p:ApiCompatGenerateSuppressionFile
```

## 🤝 Contributing
We welcome contributions! Please follow these guidelines:
- Use **Git Flow** for branch management
- Submit PRs against the `develop` branch
- Discuss major changes via GitHub issues first
- Follow existing code style and patterns

**Note:** Since v5.0, all FHIR versions (STU3+) are maintained in a single repository, simplifying contribution.

## 🆘 Support
- **Issues**: [GitHub Issues](https://github.com/FirelyTeam/firely-net-sdk/issues)
- **Discussion**: [.NET FHIR Implementers Chat on Zulip](https://chat.fhir.org/#narrow/stream/dotnet)
- **Documentation**: [Firely Documentation Site](https://docs.fire.ly)

## 📄 License
MIT License – See [LICENSE](LICENSE) for details.

---

*Part of the Firely ecosystem for FHIR implementation tools and services.*
