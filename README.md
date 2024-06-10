---
# VM Creator

VM Creator is a command-line application written in Go that reads VM specifications from an Excel file and creates those VMs in vCenter. This project is ideal for system administrators who need to automate the creation of multiple VMs with predefined specifications.

## Features

- Read VM specifications from an Excel file.
- Connect to vCenter for VM management.
- Automated creation of VMs based on the provided specifications.

## Requirements

- Go 1.16 or higher.
- Access to a vCenter environment.
- vCenter access credentials.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/eltonlaice/vm-creator.git
   cd vm-creator
   ```

2. Install dependencies:
   ```bash
   go mod tidy
   ```

## Configuration

### Excel File

Create an Excel file (`vm_specs.xlsx`) with the VM specifications. The file should have the following structure:

| Name | CPU | MemoryMB | DiskGB | Datastore | Network | Folder | Host | ResourcePool |
|------|-----|----------|--------|-----------|---------|--------|------|--------------|
| vm1  | 2   | 4096     | 20     | datastore1 | network1 | folder1 | host1 | pool1 |
| vm2  | 4   | 8192     | 40     | datastore2 | network2 | folder2 | host2 | pool2 |

### Environment Variables

Set the following environment variables with your vCenter credentials and URL:

```bash
export VCENTER_URL="https://vcenter.example.com/sdk"
export VCENTER_USERNAME="your-username"
export VCENTER_PASSWORD="your-password"
```

## Usage

To run the application, use the command:

```bash
go run main.go
```

The application will read the specifications from the `vm_specs.xlsx` file and create the VMs in vCenter according to the specifications.

## Contribution

1. Fork the project.
2. Create a branch for your feature (`git checkout -b feature/fooBar`).
3. Commit your changes (`git commit -am 'Add some fooBar'`).
4. Push to the branch (`git push origin feature/fooBar`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
