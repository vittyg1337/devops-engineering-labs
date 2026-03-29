# Lab 01 - IAM Users and Groups

## Objective

Understand how AWS Identity and Access Management separates the root account from everyday administration, and practice assigning permissions with groups and policies.

## Services Used

- AWS Identity and Access Management (IAM)
- Multi-Factor Authentication (concept review)

## What I Built

- Reviewed the difference between the AWS account root user and IAM users
- Created an IAM group for shared permission assignment
- Created IAM users for day-to-day access
- Attached permissions through group membership instead of assigning broad access directly to each user
- Reviewed least privilege and MFA as baseline security controls

## Key Concepts

The root user belongs to the AWS account itself and has unrestricted access. It should not be used for routine administration because any mistake or compromise affects the entire account.

IAM users are identities created inside the account for individual operators or workloads. They should receive only the permissions required for their job.

IAM groups simplify permission management. Instead of attaching the same policy to multiple users one by one, a group can hold the policy and users inherit access through membership.

Policies define what actions are allowed or denied on which AWS resources. AWS managed policies are useful for learning and standard roles, while customer-managed policies provide tighter control.

Least privilege means granting the minimum access needed to complete a task. This reduces risk, limits accidental changes, and is a core AWS security principle.

MFA adds a second factor beyond a password. Even if credentials are exposed, MFA makes unauthorized access significantly harder.

## Steps Performed

1. Signed in to the AWS Management Console and reviewed the account root user versus IAM user model.
2. Opened IAM and created a group for administrative or scoped access, depending on the lab goal.
3. Created one or more IAM users with console access for normal sign-in.
4. Added the users to the IAM group so permissions could be managed centrally.
5. Attached a policy to the group and validated what access the users inherited.
6. Reviewed the account security recommendations around root user protection and MFA.
7. Documented why the root account should be reserved for account-level tasks only.

## Screenshots

- Add console screenshots for user creation, group membership, and attached policies.

## What I Learned

- IAM is the control plane for identity and permissions in AWS.
- Group-based access is easier to manage and audit than assigning permissions user by user.
- Root credentials should be protected and rarely used.
- Least privilege and MFA are foundational security controls, not optional hardening steps.

## Exam Relevance

This lab maps directly to the Security and Compliance domain. It reinforces IAM, access control, MFA, and the principle of least privilege, which are core Cloud Practitioner topics.

