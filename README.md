Here’s the English translation of the text you provided:

---

# Edgetunnel
This is a script based on the CF Worker platform, modified from the original to display VLESS configuration information as subscription content. With this script, you can easily convert VLESS configuration info into formats usable by tools like Clash or Singbox via online configuration.

- **Basic Deployment Video Tutorial**: [YouTube](https://www.youtube.com/watch?v=LeT4jQUh8ok)
- **Quick Deployment Video Tutorial**: [YouTube](https://www.youtube.com/watch?v=59THrmJhmAw) ***Highly Recommended!!!***
- **Advanced Usage Video Tutorial**: [YouTube](https://www.youtube.com/watch?v=s91zjpw3-P8)
- **From Beginner to Expert Tutorial**: [YouTube](https://www.youtube.com/watch?v=oRYnrp5rQSc) ***Must Watch! Must Watch! Must Watch!!!***

Telegram Group: [@CMLiussss](https://t.me/CMLiussss), **Thanks to [Alice Networks](https://url.cmliussss.com/alice) for providing the cloud servers to maintain [CM Subscription Conversion Service](https://sub.fxxk.dedyn.io/)!**

# Disclaimer

This disclaimer applies to the "Edgetunnel" project on GitHub (hereafter referred to as "the Project"), available at: https://github.com/cmliu/edgetunnel.

### Purpose
This project is designed and developed solely for educational, research, and security testing purposes. It aims to provide security researchers, academics, and tech enthusiasts with a tool to explore and practice network communication technologies.

### Legality
When downloading and using this code, users must comply with applicable laws and regulations. Users are responsible for ensuring their actions adhere to local legal frameworks and other relevant guidelines.

### Liability
1. As the **secondary developer** of this project (referred to as "the Author"), I **cmliu** emphasize that this project is intended solely for legal, ethical, and educational purposes.
2. The Author neither endorses nor supports any form of illegal use. If this project is used for illegal or unethical activities, the Author strongly condemns it.
3. The Author is not responsible for any illegal activities conducted using this project. All consequences of using this project are the user's responsibility.
4. The Author is not liable for any direct or indirect damages resulting from the use of this project.
5. To avoid any unintended consequences or legal risks, users should delete the code within 24 hours of use.

By using this project, users acknowledge and agree to all terms of this disclaimer. If the user disagrees, they must immediately stop using the project.

The Author reserves the right to update this disclaimer at any time without notice. The latest version will be posted on the project's GitHub page.

## Risk Warnings
- Submit fake node configurations to subscription services to prevent node configuration leaks.
- You can also choose to deploy [WorkerVless2sub Subscription Generator Service](https://github.com/cmliu/WorkerVless2sub) for convenience.

## Worker Deployment Method [Video Tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=83s)

<details>
<summary><code><strong>"Workers Deployment Text Tutorial"</strong></code></summary>

1. Deploy CF Worker:
   - Create a new Worker in the CF Worker console.
   - Paste the content of [worker.js](https://github.com/cmliu/edgetunnel/blob/main/_worker.js) into the Worker editor.
   - Modify line 7 `userID` to your own **UUID**.

2. Access Subscription Content:
   - Access `https://[YOUR-WORKERS-URL]/[UUID]` to get the subscription content.
   - For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
   - For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
   - For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
   - For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` Singbox subscription format, suitable for Singbox, etc.

3. Bind Custom Domain to Workers:
   - In the Workers console, go to the `Triggers` tab and click `Add Custom Domain`.
   - Enter the subdomain you've pointed to CF DNS, e.g., `vless.google.com`, then click `Add Custom Domain`. Wait for the certificate to take effect.
   - **If you're a beginner, you can now just go ahead and don't need to read further!!!**

4. Use Your Own `Preferred Domain`/`Preferred IP` for Subscription Content:
   - If you want to use your own preferred domain or IP, refer to the [WorkerVless2sub GitHub Repository](https://github.com/cmliu/WorkerVless2sub) for deployment instructions.
   - Open the [worker.js](https://github.com/cmliu/edgetunnel/blob/main/_worker.js) file and find the `sub` variable on line 12. Modify it to the address of your deployed subscription generator. For example, `let sub = 'sub.cmliussss.workers.dev';`, make sure to remove the `https://` and other protocol symbols.
   - **Note:** If you use your own subscription address, ensure the `sub` domain and `[YOUR-WORKER-URL]` domain are in the same top-level domain; otherwise, there may be issues. You can assign the `sub` variable with the domain assigned by workers.dev.

</details>

## Pages Upload Deployment Method **Highly Recommended!!!** [Video Tutorial](https://www.youtube.com/watch?v=59THrmJhmAw)

<details>
<summary><code><strong>"Pages Upload File Deployment Text Tutorial"</strong></code></summary>

1. Deploy CF Pages:
   - Download the [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file and click on Star!!!
   - In the CF Pages console, select `Upload Assets`, give your project a name, click `Create Project`, then upload the downloaded [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file and click `Deploy Site`.
   - Once deployment is complete, click `Continue to Site`, then go to `Settings` > `Environment Variables`, define a variable for production environment > `Add Variable`.
     Variable name should be **UUID**, with the value being your UUID, then click `Save`.
   - Go back to the `Deploy` tab, click `Create New Deployment` in the bottom right, upload the [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file again and click `Save and Deploy`.

2. Access Subscription Content:
   - Access `https://[YOUR-PAGES-URL]/[YOUR-UUID]` to get the subscription content.
   - For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
   - For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
   - For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
   - For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` Singbox subscription format, suitable for Singbox, etc.

3. Bind CNAME Custom Domain to Pages: [Video Tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=851s)
   - In the Pages console's `Custom Domain` tab, click `Set Custom Domain`.
   - Enter your custom subdomain (don't use your root domain), for example:
     If your domain is `fuck.cloudns.biz`, then enter `lizi.fuck.cloudns.biz` as the custom domain.
   - Follow CF's instructions to add the CNAME record `edgetunnel.pages.dev` to your DNS provider for the domain `lizi`, then click `Activate Domain`.
   - **If you're a beginner, after binding your Pages custom domain, you're ready to go!**

4. Use Your Own `Preferred Domain`/`Preferred IP` for Subscription Content:
   - If you want to use your own preferred domain or IP, refer to the [WorkerVless2sub GitHub Repository](https://github.com/cmliu/WorkerVless2sub) for deployment instructions.
   - In the Pages console's `Settings` tab, go to `Environment Variables` > `Create` > `Edit Variable` > `Add Variable`.
   - Set the variable name to `SUB` with the value of your subscription generator address. For example,
