name: chapter-1
class: title, shelf, no-footer, fullbleed
background-image: url(https://hashicorp.github.io/field-workshops-assets/assets/bkgs/HashiCorp-Title-bkg.jpeg)
count: false

# Chapter 1  
## HashiCorp Vault Overview

![:scale 15%](https://hashicorp.github.io/field-workshops-assets/assets/logos/logo_vault.png)

???
Chapter 1 introduces Vault

---
name: hashiCorp-vault-overview
# HashiCorp Vault Overview
![:scale 10%](https://hashicorp.github.io/field-workshops-assets/assets/logos/logo_vault.png)

  * HashiCorp Vault�́AAPI�哱�̃N���E�h�s�m�̔閧�Ǘ��V�X�e���ł��B
  * �n�C�u���b�h�N���E�h���ŃZ���V�e�B�u�ȃf�[�^�����S�ɕۑ��E�Ǘ����邱�Ƃ��ł��܂��B
  * Vault ���g�p���āA���I�ɒZ���̃N���f���V�����𐶐�������A�A�v���P�[�V�����̃f�[�^�����̏�ňÍ��������肷�邱�Ƃ��ł��܂��B

???
This is meant as a high level overview.  For detailed descriptions or instructions please see the docs, API guide, or learning site:
* https://www.vaultproject.io/docs/
* https://www.vaultproject.io/api/
* https://learn.hashicorp.com/vault/

---
name: the-old-way
layout: false
# The Traditional Security Model
.center[![:scale 70%](images/bodiam_castle.jpg)]
.center[�ʖ��u��Ɩx�@�v�Ƃ��Ă΂�Ă��܂��B"Castle and Moat"]

???
* This picture shows the traditional castle and moat security model.

---
layout: true

.footer[
- Copyright © 2019 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: traditional-security-models
# The Traditional Security Model
* �]���̃Z�L�����e�B���f���́A���E���Ɋ�Â����Z�L�����e�B�̍l���Ɋ�Â��č\�z����Ă��܂����B
* �t�@�C�A�E�H�[��������A���̒��ł͈��S���Ǝv���Ă��܂����B
* �f�[�^�x�[�X�Ȃǂ̃��\�[�X�́A�قƂ�ǂ��ÓI�Ȃ��̂ł����B ���̂悤�ȃ��[���� IP �A�h���X�Ɋ�Â��Ă���A�N���f���V�����̓\�[�X�R�[�h�ɑg�ݍ��܂�Ă�����A�f�B�X�N��̐ÓI�t�@�C���ɕۑ�����Ă��܂����B

???
This slide discusses the traditional security model

---
name: problems-with-traditional-security-models
# Problems with the Traditional Security Model
* IP�A�h���X�x�[�X�̃��[��
* ���̂悤�Ȗ��̂���n�[�h�R�[�h���ꂽ���i���B
  * �A�v���ƃ��[�U�[�̋��L�T�[�r�X�A�J�E���g
  * ��]��������A�p�F�ɂ�����A�N���A�N�Z�X�ł��邩�𔻒f����͓̂���B
  * ��w���������i�������������Ƃ��ł���

???
* This slide describes some of the problems with the traditional security model.
---
name: the-new-way
layout: false
# Modern Secrets Management
.center[![:scale 65%](images/nomadic_houses.jpg)]
.center[�\���ɒ�`���ꂽ���E�����Ȃ����߁A�A�C�f���e�B�e�B�ɂ���ăZ�L�����e�B����������Ă��܂��B]

???
* These are Mongolian Yurts or "Ger" as they are called locally. Instead of a castle with walls and a drawbridge, a fixed fortress that has an inside and an outside, these people move from place to place, bringing their houses with them.

* And if you don't think the Nomadic way can be an effective security posture, think about this for a moment. The Mongol military tactics and organization enabled the Genghis Khan to conquer nearly all of continental Asia, the Middle East and parts of eastern Europe. Mongol warriors would typically bring three or four horses with them, so they could rotate through the horses and go farther. Mongol army units could move up to 100 miles a day, which was unheard of in the 13th century. They were faster, more adaptable, and more resilient than all their enemies.

---
name: identity-based-security-1
#Identity Based Security
.center[![:scale 75%](images/identity-triangle.png)]
.center[[Identity Based Security and Low Trust Networks](https://www.hashicorp.com/identity-based-security-and-low-trust-networks)
]

???
* Here we see that Vault has multiple means of authenticating users and applications with its Auth Methods.
* Vault can manage many types of secrets and excels at generating short-lived, dynmamic secrets.
* Vault's ACL policies are associated with tokens that users and applications use to access secrets after authenticating.
* Tokens can only read/write secrets that its policies allow.
* Click on the link to read a white paper about identity-based security in low trust networks.

---
layout: true

.footer[
- Copyright © 2019 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: identity-based-security-2
# Identity Based Security

Vault�́A����̃A�v���P�[�V�����̃Z�L�����e�B�j�[�Y�ɑΏ����邽�߂ɐ݌v����܂����B ���̎g�p���́A�]���̃A�v���[�`�Ƃ͈قȂ�܂��B

* �A�C�f���e�B�e�B�x�[�X�̃��[���ɂ��A�l�b�g���[�N�̋��E���z���ăZ�L�����e�B���g�����邱�Ƃ��ł��܂��B
* �p�ɂɃ��[�e�[�V���������_�C�i�~�b�N�ŒZ���Ȏ��i���
* �����̃A�J�E���g�ł��G���e�B�e�B�ɂ���ĒP�ꃆ�[�U�[�Ƃ��Ĉ�����
* �ȒP�ɖ����������\���̂��鎑�i���ƃG���e�B�e�B

???
* This slide discusses how Vault is designed for modern applications.

---
name: secrets-engines
layout: false
# Vault Secrets Engines
.center[![:scale 60%](images/vault-engines.png)]
.center[[Vault Secrets Engines](https://www.vaultproject.io/docs/secrets/)]

???
* Vault provides many out-of-the-box secrets engines.
* Additional custom secrets engines can be added by customers.
* Click on the link to learn more about Vault secrets engines.

---
name: vault-reference-architecture-1
# Vault Architecture Internals
.center[![:scale 75%](images/vault_arch.png)]
.center[[HashiCorp Vault Internals Architecture](https://www.vaultproject.io/docs/internals/architecture/)
]

???
* Click the link to learn more about the internal's of Vault's architecture.

---
name: vault-reference-architecture-2
# Vault Architecture - High Availability
.center[![:scale 60%](images/vault-ref-arch-lb.png)]
.center[[Vault High Availability](https://www.vaultproject.io/docs/concepts/ha/)
]

???
* Vault allows multiple servers to be combined in a highly available cluster within a single cloud region or physical data center.
* Click on the link to learn more about Vault's high availability in a single cluster.

---
name: vault-reference-architecture-3
# Vault Architecture - Multi-Region
.center[![:scale 70%](images/vault-ref-arch-replication.png)]
.center[[Vault Enterprise Replication](https://www.vaultproject.io/docs/enterprise/replication/)
]

???
* Vault Enterprise supports replication between clusters across regions and data centers.
* It supports Disaster Recovery and Performance replication.
* These can be used together.
* Click the link to learn more about Vault's replication.

---
layout: true

.footer[
- Copyright © 2019 HashiCorp
- ![:scale 100%](https://hashicorp.github.io/field-workshops-assets/assets/logos/HashiCorp_Icon_Black.svg)
]

---
name: chapter-1-review-question
# 📝 Chapter 1 Review

* What is HashiCorp Vault?

???
* Let's review what we learned in this chapter.
---
name: chapter-1-review-answer
# 📝 Chapter 1 Review
* What is HashiCorp Vault?
 * Vault�̓V�[�N���b�g�Ǘ��V�X�e���ł��B
  * API�쓮�^�ŁA�N���E�h�Ɉˑ����܂���B
  * �M������Ă��Ȃ��l�b�g���[�N�Ŏg�p���邱�Ƃ��ł��܂��B
  * �����̃V�X�e���ɑ΂��ă��[�U�[��A�v���P�[�V������F�؂��邱�Ƃ��ł��܂��B
  * �Z���ȃV�[�N���b�g�̓��I�������T�|�[�g���܂��B
  * �n����܂����ŕ����\�ȁA���p�\���̍����N���X�^�œ��삵�܂��B

???
* Here are the answers to the review questions.
