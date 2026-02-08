# Agent Capabilities

The Ansible Connection Analyzer can reason about the following areas:

---

## Connection Types

- SSH (Linux / Unix hosts)
- WinRM (Windows hosts)

---

## Error Categories

- Host unreachable
- Connection timeout
- Authentication failure
- Incorrect port or protocol
- Inventory misconfiguration

---

## Inputs It Understands

- Ansible error output
- Inventory variables (e.g. ansible_host, ansible_user, ansible_port)
- Connection method indicators

---

## Reasoning Signals

- Error message patterns
- Network vs authentication symptoms
- Inventory and protocol mismatches
