    <section class="filter-content" markdown="1" data-scope="mac">
    {% include_cached copy-clipboard.html %}
    ~~~ shell
    cockroach sql --url 'postgresql://<username>:<password>@<serverless-host>:26257/defaultdb?sslmode=verify-full&sslrootcert='$HOME'/.postgresql/root.crt&options=--cluster=<cluster-name>-<tenant-id>'
    ~~~
    </section>

    <section class="filter-content" markdown="1" data-scope="linux">
    {% include_cached copy-clipboard.html %}
    ~~~ shell
    cockroach sql --url 'postgresql://<username>:<password>@<serverless-host>:26257/defaultdb?sslmode=verify-full&sslrootcert='$HOME'/.postgresql/root.crt&options=--cluster=<cluster-name>-<tenant-id>'
    ~~~
    </section>

    <section class="filter-content" markdown="1" data-scope="windows">
    {% include_cached copy-clipboard.html %}
    ~~~ shell
    cockroach sql --url "postgresql://<username>:<password>@<serverless-host>:26257/defaultdb?sslmode=verify-full&sslrootcert=$env:appdata/.postgresql/root.crt&options=--cluster=<cluster-name>-<tenant-id>"
    ~~~
    </section>

    Where:
    - `<username>` is the SQL user. By default, this is your {{ site.data.products.db }} account username.
    - `<password>` is the password for the SQL user. The password will be shown only once in the **Connection info** dialog after creating the cluster.
    - `<serverless-host>` is the hostname of the {{ site.data.products.serverless }} cluster.
    - `<cluster-name>-<tenant-id>` is the short name of your cluster plus the tenant ID. For example, `funny-skunk-123`. The `<tenant-id>` is used to identify your tenant cluster on a multitenant host.
    - `<cluster-id>` is a unique string used to identify your cluster when downloading the CA certificate. For example, `12a3bcde-4fa5-6789-1234-56bc7890d123`.

    You can find these settings in the **Connection parameters** tab of the **Connection info** dialog.