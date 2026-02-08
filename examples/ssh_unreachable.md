# Example: SSH Host Unreachable

## Input

fatal: [web01]: UNREACHABLE! => {
"changed": false,
"msg": "Failed to connect to the host via ssh: No route to host",
"unreachable": true
}


Inventory snippet:

web01 ansible_host=192.0.2.10 ansible_user=admin


---

## Analysis

- SSH connection could not be established
- Error indicates a network-level reachability issue
- Inventory specifies a static IP address

---

## Output

**Summary:**  
Ansible failed to reach the target host over SSH.

**Likely Root Cause:**  
The specified host address is unreachable from the control node.

**Supporting Evidence:**  
The error message reports "No route to host", which indicates a network path issue rather than authentication.

**Suggested Fix:**  
Verify the target IP address and network connectivity, or update `ansible_host` with the correct value.

