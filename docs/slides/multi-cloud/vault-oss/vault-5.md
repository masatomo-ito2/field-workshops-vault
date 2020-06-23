name: chapter-5
class: title, shelf, no-footer, fullbleed
background-image: url(https://hashicorp.github.io/field-workshops-assets/assets/bkgs/HashiCorp-Title-bkg.jpeg)
count: false

# Chapter 5      
## Vault Authentication Methods

![:scale 15%](https://hashicorp.github.io/field-workshops-assets/assets/logos/logo_vault.png)

???

* Chapter 5 introduces Vault authentication methods
* It focuses on the Userpass method.

---
layout: true

.footer[
- Copyright 2019 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: vault-auth-methods
# Vault Authentication Methods
.center[![:scale 45%](images/vault_auth_methods.png)]
.center[Vault�͑�����Auth method���T�|�[�g���Ă��܂��B]

???
* Auth methods are how your apps and users verify their identity.
* In the same way you might present some kind of valid ID at the hotel check-in desk, users and apps provide some kind of credential or token to authenticate.
* You can enable multiple auth methods and multiple instances of the same auth method.

---
name:vault-auth-methods-2
# Some Important Vault Auth Methods

<div style="float: left; width: 50%;">
<u>Methods for Users</u>
<ul>
<li>Userpass</li>
<li>GitHub</li>
<li>LDAP</li>
<li>JWT/OIDC</li>
<li>Okta</li>
</ul>
</div>
<div style="float: right; width: 50%;">
<u>Methods for Applications</u>
<ul>
<li>AppRole</li>
<li>AWS</li>
<li>Azure</li>
<li>Google Cloud</li>
<li>Kubernetes</li>
</ul>
</div>

???
* Userpass - Allows users to authenticate with username and password managed by Vault
* GitHub - Allows users to authenticate with their GitHub personal access tokens
* LDAP - Allows users to authenticate against an LDAP server with their username and password managed by that server.
* JWT/OIDC - Allows users to authenticate against an external OpenID Connect provider or with JSON Web Tokens (JWTs)
* Okta - Allows users to authenticate using Okta single sign-on.
* AppRole - Allows applications to authenticate in automated workflows using a role and a role ID.
* AWS - Allows applications on AWS EC2 instances and Lambda functions to authenticate with IAM credentials or EC2 metadata.
* Azure - Allows applications associated with Azure Managed Service Identities to authenticate using Azure Active Directory credentials.
* Google Cloud - Allows applications in GCP to authenticate using Google Cloud IAM service accounts or Google Compute Engine (GCE) metadata.
* Kubernetes - Allows Kubernetes pods to authenticate with JWT tokens.

---
name: enabling-auth-methods
# Enabling Authentication Methods

* Vault auth methods�͖����I�ɗL���ɂ��܂��B
	* `vault auth enable`�ōs���܂��B
* �eauth method�̓f�t�H���g��Path������܂��B
* �ʂ�Path���ݒ�\�ł��B
	* `vault auth enable -path=aws-east aws`
* �J�X�^��Path��CLI��API�ŃA�N�Z�X���܂��B
	* �J�X�^���p�X�F `vault write aws-east/config/root`
	* �f�t�H���g�F `vault write aws/config/root`

???

* Talk about enabling auth methods.
* Talk about default and custom paths
* Explain the examples

---
name: userpass-0
# Vault's Userpass Auth Method
.center[![:scale 30%](images/userpass_login.png)]
* Userpass ���\�b�h�́AVault ���Ǘ����郆�[�U�[���ƃp�X���[�h�Ń��[�U�[��F�؂��܂��B

???
* The Userpass method allows users to authenticate with username and password managed by Vault.
* It is not recommended for production, but it's fine for development and lab environments.
* In the real world you'd probably have Vault use your Active Directory, LDAP, GitHub, or other system of record for authentication by users.

---
name: lab-vault-basics-challenge-6
# Lab Challenge 5.1: Userpass Auth Method
* In this lab, you'll enable and use the Userpass auth method.
* Instructions:
  * Click the "Use the Userpass Auth Method" challenge of the "Vault Basics" track.
  * Then click the green "Start" button.
  * Follow the challenge's instructions.
  * Click the green "Check" button when finished.

???
* Instruct the students to do the "Use the Userpass Auth Method" challenge of the "Vault Basics" track.
* This challenge has them enable an instance of the Userpass auth method.
* It also demonstrates that Vault is "deny by default" since the Userpass user that they create will not have any access to secrets yet.

---
name: chapter-5-review-questions
# Chapter 5 Review
* Vault �ł́A�ǂ̂悤�Ȏ�ނ̃G���e�B�e�B��F�؂ł��܂����H
* Userpass �F�ؕ��@�̎��i���́A�ǂ̂悤�ȃV�X�e���ŊǗ�����Ă��܂����H
* �f�t�H���g�̃|���V�[�ȊO�̃|���V�[�����蓖�Ă��Ă��Ȃ����[�U�[�́A�V�[�N���b�g�ɃA�N�Z�X�ł��܂����H


???
* Let's review what we learned in this chapter.

---
name: chapter-5-review-answers
# Chapter 5 Review

* Vault �́A�ǂ̂悤�Ȏ�ނ̃G���e�B�e�B��F�؂ł��܂����H
  * ���[�U�[����уA�v���P�[�V����
* Userpass auth ���\�b�h�̔F�؏����Ǘ�����V�X�e���͉��ł���?
  * Vault
* �f�t�H���g�|���V�[�ȊO�̃|���V�[�����蓖�Ă��Ă��Ȃ����[�U�[�́A�V�[�N���b�g�ɃA�N�Z�X�ł��܂���?
  * ������


???
* Here are the answers to the review questions.
