# Request GPU access on Jupyter4NFDI

## Learning objectives

By the end of this lesson, you will be able to:

- Prepare a clear GPU access request.
- Follow the registration and login process via Helmholtz ID.
- Troubleshoot common login and access issues.


## 1. Request access

GPU access is not enabled for every account by default. You must request it separately.

Email **jupyter4nfdi AT lists.nfdi.de** and include:

1. What you want to do with a GPU (research project, learning, ML training or other use case).
2. How long you expect to need GPU access.
3. Any requirements, such as software or estimated memory requirements, and any questions.

The Jupyter4NFDI team **typically responds within 1-2 business days**. Note that this is guidance, not a guaranteed approval time.


## 2. Look for the Helmholtz ID invitation

Once access is approved, expect an email invitation from **Helmholtz ID**, the Helmholtz identity management system. Its text may refer to a group or a virtual organisation (VO). Follow **all invitations actually sent to you**.

Typical invitation wording includes:

> You are invited to the group (VO) [group name] on Helmholtz ID.

The invitation includes a **personal registration link and expiry date** (often only a few days). Open the link and follow the instructions. If your link expires, contact the **administrator of the VO** to request a new invitation; generally only the group administrator can resend it. If you do not know who that is, contact the Jupyter4NFDI team.

## 3. Use the same Helmholtz ID identity for both steps

**This is essential:** accept the invitation using the **same Helmholtz ID login / underlying identity provider account** you use when you sign in to Jupyter4NFDI.

If you already have a Helmholtz ID account, the invitation page may offer a **login link above the list of organisations**. Choose that option instead of creating a second identity.

Jupyter4NFDI can also be accessed through other community AAIs via the NFDI Infrastructure Proxy. However, **GPU group membership in this current workflow is held in Helmholtz ID**. If you log into Jupyter4NFDI through a different community AAI (for example, Academic Cloud) that does not transmit the relevant entitlement, the GPU profiles may **not** appear—even after you have accepted the Helmholtz ID invitation.

**To avoid this:** log out of Jupyter4NFDI, select **Helmholtz ID** through the NFDI Infrastructure Proxy, and use the same underlying identity as for your invitation. A Helmholtz ID login can itself delegate to your institutional or social identity provider. See the [authentication guide](https://nfdi-jupyter.de/authentication/).

## 4. Finish registration

After you have followed the invitation, you may receive a second email similar to:

> Your account in Helmholtz ID ... is now ready to use. Please go ahead and use the connected service(s).

**This confirmation means your Helmholtz ID account is ready.** It does not on its own guarantee that GPU resources have been provisioned and are immediately available.

Now sign in to [Jupyter4NFDI](https://hub.nfdi-jupyter.de/hub/home), using the correct Helmholtz ID path, and check the available server profiles. If your session was already active, sign out and log in again so fresh group attributes can be received.

## Troubleshooting

| Problem | What to do |
| --- | --- |
| Invitation link expired | Contact the VO administrator to request a new invitation. |
| Invitation accepted with a different identity | Ask Jupyter4NFDI support to verify the correct group membership / identity mapping. |
| You see ordinary Jupyter servers but no GPU choices | Check whether you used Helmholtz ID rather than another community AAI; sign out and back in. |
| An approved GPU profile appears but cannot start | Shared GPU capacity may be exhausted. Try again later or contact support. |
| You see a GPU profile but Python cannot detect CUDA | Check the actual server profile, kernel environment and installed GPU-compatible libraries in the next lesson. |


**Next:** [Explore GPU computing without a GPU](03_cpu_demo.md).
