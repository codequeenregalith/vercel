import React from 'react';

export default function Home() {
  return (
    <div className="min-h-screen bg-gray-900 text-white font-sans">
      {/* Header */}
      <header className="flex justify-between items-center px-8 py-6 border-b border-gray-700">
        <h1 className="text-3xl font-bold tracking-wide">Cypher Courses</h1>
        <nav className="space-x-6">
          <a href="#courses" className="hover:text-teal-400 transition">Courses</a>
          <a href="#about" className="hover:text-teal-400 transition">About</a>
          <a href="#contact" className="hover:text-teal-400 transition">Contact</a>
        </nav>
      </header>

      {/* Hero */}
      <section className="text-center py-20 px-6">
        <h2 className="text-5xl md:text-6xl font-extrabold mb-6">Build Your Business Without Burning Out</h2>
        <p className="max-w-2xl mx-auto text-lg text-gray-300 mb-8">
          Cypher Courses empowers young entrepreneurs with practical business & finance skills, uniquely integrated with well-being strategies for sustainable success.
        </p>
        <div className="flex justify-center gap-6">
          <a href="https://wa.me/252624241927?text=Hi,%20I%20want%20to%20enroll%20in%20Cypher%20Courses" target="_blank" rel="noopener noreferrer" className="bg-teal-500 hover:bg-teal-400 text-black font-semibold px-6 py-3 rounded-2xl shadow-lg transition">Message on WhatsApp</a>
          <a href="#" className="bg-gray-700 hover:bg-gray-600 text-white font-semibold px-6 py-3 rounded-2xl shadow-lg transition">Join Discord (Coming Soon)</a>
        </div>
      </section>

      {/* Courses Section */}
      <section id="courses" className="px-6 md:px-16 py-20">
        <h3 className="text-3xl font-bold mb-10 text-center">Our Courses</h3>
        <div className="grid md:grid-cols-3 gap-8">
          <div className="bg-gray-800 p-6 rounded-2xl shadow-md hover:scale-105 transition">
            <h4 className="text-xl font-semibold mb-2">Startup Foundations</h4>
            <p className="text-gray-300 mb-4">Learn how to turn your ideas into a profitable business with step-by-step strategies.</p>
            <span className="block text-teal-400 font-bold mb-2">Monthly: €44.99</span>
            <span className="block text-teal-400 font-bold mb-4">Annual: €109.99</span>
            <a href="https://wa.me/252624241927?text=Hi,%20I%20want%20to%20enroll%20in%20Startup%20Foundations" target="_blank" rel="noopener noreferrer" className="text-teal-400 hover:underline">Buy Now →</a>
          </div>
          <div className="bg-gray-800 p-6 rounded-2xl shadow-md hover:scale-105 transition">
            <h4 className="text-xl font-semibold mb-2">Finance Made Simple</h4>
            <p className="text-gray-300 mb-4">Master budgeting, investing, and scaling without the overwhelm.</p>
            <span className="block text-teal-400 font-bold mb-2">Monthly: €44.99</span>
            <span className="block text-teal-400 font-bold mb-4">Annual: €109.99</span>
            <a href="https://wa.me/252624241927?text=Hi,%20I%20want%20to%20enroll%20in%20Finance%20Made%20Simple" target="_blank" rel="noopener noreferrer" className="text-teal-400 hover:underline">Buy Now →</a>
          </div>
          <div className="bg-gray-800 p-6 rounded-2xl shadow-md hover:scale-105 transition">
            <h4 className="text-xl font-semibold mb-2">Well-being for Entrepreneurs</h4>
            <p className="text-gray-300 mb-4">Build habits and strategies to protect your mental health while growing your empire.</p>
            <span className="block text-teal-400 font-bold mb-2">Monthly: €44.99</span>
            <span className="block text-teal-400 font-bold mb-4">Annual: €109.99</span>
            <a href="https://wa.me/252624241927?text=Hi,%20I%20want%20to%20enroll%20in%20Well-being%20for%20Entrepreneurs" target="_blank" rel="noopener noreferrer" className="text-teal-400 hover:underline">Buy Now →</a>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="px-6 md:px-16 py-20 bg-gray-950">
        <div className="max-w-3xl mx-auto text-center">
          <h3 className="text-3xl font-bold mb-6">Why Cypher?</h3>
          <p className="text-gray-300 text-lg">Most entrepreneurship platforms teach hustle only. Cypher blends business mastery with well-being so you can achieve sustainable success without burnout.</p>
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="text-center py-10 border-t border-gray-700">
        <p className="text-gray-400">© {new Date().getFullYear()} Cypher Courses. All rights reserved.</p>
        <div className="mt-2 flex justify-center gap-4">
          <a href="https://wa.me/252624241927" target="_blank" rel="noopener noreferrer" className="text-teal-400 hover:underline">WhatsApp</a>
          <a href="#" className="text-teal-400 hover:underline">Instagram</a>
        </div>
      </footer>
    </div>
  );
}

Please read our [Code of Conduct](./.github/CODE_OF_CONDUCT.md) and follow it in all your interactions with the project.

### Local development

This project is configured in a monorepo, where one repository contains multiple npm packages. Dependencies are installed and managed with `pnpm`, not `npm` CLI.

To get started, execute the following:

```
git clone https://github.com/vercel/vercel
cd vercel
corepack enable
pnpm install
pnpm build
pnpm lint
pnpm test-unit
```

Make sure all the tests pass before making changes.

#### Running Vercel CLI Changes

You can use `pnpm vercel` from the `cli` package to invoke Vercel CLI with local changes:

```
cd ./packages/cli
pnpm vercel <cli-commands...>
```

See [CLI Local Development](../packages/cli#local-development) for more details.

### Verifying your change

Once you are done with your changes (we even suggest doing it along the way), make sure all the tests still pass by running:

```
pnpm test-unit
```

from the root of the project.

If any test fails, make sure to fix it along with your changes. See [Interpreting test errors](#Interpreting-test-errors) for more information about how the tests are executed, especially the integration tests.

### Pull Request Process

Once you are confident that your changes work properly, open a pull request on the main repository.

The pull request will be reviewed by the maintainers and the tests will be checked by our continuous integration platform.

### Interpreting test errors

There are 2 kinds of tests in this repository – Unit tests and Integration tests.

Unit tests are run locally with `jest` and execute quickly because they are testing the smallest units of code.

#### Integration tests

Integration tests create deployments to your Vercel account using the `test` project name. After each test is deployed, the `probes` key is used to check if the response is the expected value. If the value doesn't match, you'll see a message explaining the difference. If the deployment failed to build, you'll see a more generic message like the following:

```
[Error: Fetched page https://test-8ashcdlew.vercel.app/root.js does not contain hello Root!. Instead it contains An error occurred with this application.

    NO_STATUS_CODE_FRO Response headers:
       cache-control=s-maxage=0
      connection=close
      content-type=text/plain; charset=utf-8
      date=Wed, 19 Jun 2019 18:01:37 GMT
      server=now
      strict-transport-security=max-age=63072000
      transfer-encoding=chunked
      x-now-id=iad1:hgtzj-1560967297876-44ae12559f95
      x-now-trace=iad1]
```

In such cases, you can visit the URL of the failed deployment and append `/_logs` to see the build error. In the case above, that would be https://test-8ashcdlew.vercel.app/_logs

The logs of this deployment will contain the actual error which may help you to understand what went wrong.

##### Running integration tests locally

While running the full integration suite locally is not recommended, it's sometimes useful to isolate a failing test by running it on your machine. To do so, you'll need to ensure you have the appropriate credentials sourced in your shell:

1. Create an access token. Follow the instructions here https://vercel.com/docs/rest-api#creating-an-access-token. Ensure the token scope is for your personal
   account.
2. Grab the team ID from the Vercel dashboard at `https://vercel.com/<MY-TEAM>/~/settings`.
3. Source these into your shell rc file: `echo 'export VERCEL_TOKEN=<MY-TOKEN> VERCEL_TEAM_ID=<MY-TEAM-ID>' >> ~/.zshrc`

From there, you should be able to trigger an integration test. Choose one
that's already isolated to check that things work:

```
cd packages/next
```

Run the test:

```
pnpm test test/fixtures/00-server-build/index.test.js
```

> [!NOTE]
> If you receive a `401` status code while fetching the deployment, you need to disable [Deployment Protection](https://vercel.com/docs/security/deployment-protection) on the project.

#### @vercel/nft

Some of the Builders use `@vercel/nft` to tree-shake files before deployment. If you suspect an error with this tree-shaking mechanism, you can create the following script in your project:

```js
const { nodeFileTrace } = require('@vercel/nft');
nodeFileTrace(['path/to/entrypoint.js'], {
  ts: true,
  mixedModules: true,
})
  .then(o => console.log(o.fileList))
  .then(e => console.error(e));
```

When you run this script, you'll see all the imported files. If files are missing, the bug is in [@vercel/nft](https://github.com/vercel/nft) and not the Builder.

### Deploy a Builder with existing project

Sometimes you want to test changes to a Builder against an existing project, maybe with `vercel dev` or actual deployment. You can avoid publishing every Builder change to npm by uploading the Builder as a tarball.

1. Change directory to the desired Builder `cd ./packages/node`
2. Run `pnpm build` to compile typescript and other build steps
3. Run `npm pack` to create a tarball file
4. Run `vercel *.tgz` to upload the tarball file and get a URL
5. Edit any existing `vercel.json` project and replace `use` with the URL
6. Run `vercel` or `vercel dev` to deploy with the experimental Builder

## Reference

- [Code of Conduct](./.github/CODE_OF_CONDUCT.md)
- [Contributing Guidelines](./.github/CONTRIBUTING.md)
- [Apache 2.0 License](./LICENSE)
