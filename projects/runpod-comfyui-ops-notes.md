## Runpod ComfyUI Template Environment Setup

This document outlines the necessary configurations for running web applications (like `Vue.js`) within a `Runpod ComfyUI Template` environment and accessing them from an external web browser. It provides clear instructions for setting up port access and verifying local app execution.

`RunPod` instances run on **Linux (typically Ubuntu)**, so all bash commands shown in this guide will work directly in the **JupyterLab terminal**.

> ⚠️ **Note:** These configurations are crucial for making your web app accessible from outside the `RunPod` instance.

---

### 1. Add HTTP Port (During Runpod Deployment)

When you `Deploy` a `RunPod` instance, the following steps are crucial for external access:

*   Explicitly add the port number (e.g., `5173`) that your web application will use. If this port is not added, RunPod's firewall will block access, resulting in an `Access Denied` error.
*   **Action for Access Denied:** If you encounter an `Access Denied` error, double-check your `RunPod` instance's `HTTP` port configuration in the RunPod console and ensure the required port is listed.

---

### 2. Verify Vue.js App Locally (Within RunPod)

This step is for running and testing your Vue app **within the RunPod environment itself**.

> **Note on Ports:** For simplicity, we will use the same port, `5173`, in this example. You can use any port you like, as long as it's the same one you exposed in Step 1.

#### Check Port Status:

Before running your app, verify that the port is not already in use.

```bash
# Check if port 5173 is in use
ss -tlnp | grep 5173
```

#### Run Vue Development Server

Execute the following command to start the Vue development server. This configures it to listen on all network interfaces (`0.0.0.0`) and a specific port (in this case, `5173`). This allows you to access the app from within the `RunPod` environment by visiting `localhost:5173` in the built-in browser or using the `JupyterLab Open Port` feature.

> ⚙️ **Important:** Ensure you run this command from your **`Vue.js` project’s root directory**.

```bash
# Start the Vue development server on port 5173
npm run dev -- --host 0.0.0.0 --port 5173
```
