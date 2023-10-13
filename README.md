## About
This is the "single source of truth" that stores all my articles.

It utilizes [huantt/article-as-code](https://github.com/huantt/article-as-code) to collect, store, and sync all my articles to various platforms, including [dev.to](https://dev.to) and [hashnode.dev](https://hashnode.dev).

## GitHub Action
I have created a GitHub action in the `.github/workflows` directory that runs every 6 hours or whenever you commit to the `main` branch.

## My Recent Articles

<table>
        <tr>
            <td width="300px">
                <a href="https://dev.to/aws-builders/how-netflix-uses-the-cloud-aws-191c">
                    <img src="https://dynamic-thumbnail-dev-to.vercel.app/article/1581112/thumbnail?t=2023-10-13%2018%3a27%3a20.131364137%20%2b0000%20UTC%20m%3d%2b0.073613757" alt="thumbnail">
                </a>
            </td>
            <td>
                <a href="https://dev.to/aws-builders/how-netflix-uses-the-cloud-aws-191c">How Netflix Uses the Cloud - AWS</a>
                <div>How they Use AWS Services   Binge-watching 🍿has become more and more of a phenomena. Netflix...</div>
                <div><i>27/08/2023</i></div>
            </td>
        </tr>
        <tr>
            <td width="300px">
                <a href="https://dev.to/aws-builders/every-project-deserves-its-cicd-pipeline-no-matter-how-small-19j9">
                    <img src="https://dynamic-thumbnail-dev-to.vercel.app/article/1582032/thumbnail?t=2023-10-13%2018%3a27%3a20.131364137%20%2b0000%20UTC%20m%3d%2b0.073613757" alt="thumbnail">
                </a>
            </td>
            <td>
                <a href="https://dev.to/aws-builders/every-project-deserves-its-cicd-pipeline-no-matter-how-small-19j9">Every Project Deserves its CI/CD pipeline, no matter how small</a>
                <div>TL;DR   In today&#39;s tech industry, setting up a CI/CD pipeline is quite easy. Creating a...</div>
                <div><i>28/08/2023</i></div>
            </td>
        </tr>
        <tr>
            <td width="300px">
                <a href="https://dev.to/softwaresennin/create-your-first-web-app-using-chatgpt-2174">
                    <img src="https://dynamic-thumbnail-dev-to.vercel.app/article/1574302/thumbnail?t=2023-10-13%2018%3a27%3a20.131364137%20%2b0000%20UTC%20m%3d%2b0.073613757" alt="thumbnail">
                </a>
            </td>
            <td>
                <a href="https://dev.to/softwaresennin/create-your-first-web-app-using-chatgpt-2174">Create your first Web-app using ChatGPT</a>
                <div>Introduction   Language translation is essential in our globalized world, bridging language...</div>
                <div><i>21/08/2023</i></div>
            </td>
        </tr>
        <tr>
            <td width="300px">
                <a href="https://dev.to/aws-builders/localstack-emulate-aws-services-for-local-development-testing-eoj">
                    <img src="https://dynamic-thumbnail-dev-to.vercel.app/article/1545036/thumbnail?t=2023-10-13%2018%3a27%3a20.131364137%20%2b0000%20UTC%20m%3d%2b0.073613757" alt="thumbnail">
                </a>
            </td>
            <td>
                <a href="https://dev.to/aws-builders/localstack-emulate-aws-services-for-local-development-testing-eoj">LocalStack: Emulate AWS Services for Local Development &amp; Testing</a>
                <div>It can be time-consuming, difficult, and even dangerous to create and test cloud-based apps in a...</div>
                <div><i>22/07/2023</i></div>
            </td>
        </tr>
        <tr>
            <td width="300px">
                <a href="https://dev.to/softwaresennin/k8s-quickstart-helm-566o">
                    <img src="https://dynamic-thumbnail-dev-to.vercel.app/article/1573621/thumbnail?t=2023-10-13%2018%3a27%3a20.131364137%20%2b0000%20UTC%20m%3d%2b0.073613757" alt="thumbnail">
                </a>
            </td>
            <td>
                <a href="https://dev.to/softwaresennin/k8s-quickstart-helm-566o">K8S Quickstart &amp; Helm</a>
                <div>Today, Kubernetes becomes a must for DevOps Engineers, SRE and others for orchestrating containers....</div>
                <div><i>20/08/2023</i></div>
            </td>
        </tr>
</table>

<div align="right">

*Updated at: 2023-10-13T18:27:20Z - by **[huantt/article-listing](https://github.com/huantt/article-listing)***

</div>


## Run Locally
The `docker-compose.yml` file helps us run the flow locally.

To run this Docker Compose, create a `.secret.txt` file and fill in the following variables:
- `DEVTO_TOKEN`: Your Dev.to authentication token.
- `DEVTO_USERNAME`: Your Dev.to username.
- `HASHNODE_TOKEN`: Your Hashnode authentication token.
- `HASHNODE_USERNAME`: Your Hashnode username.

Run the following command:
```shell
docker-compose up
```

## Sequence Diagram
```mermaid
sequenceDiagram
This repo ->> Dev.to: Get articles
Dev.to -->> This repo: Articles
This repo ->> This repo: Store articles as code
This repo ->> Dev.to: Sync articles
This repo ->> Hashnode.dev: Sync articles
This repo ->> Github: Commit
```