# Rename This Repository

## Problem

The current name `KitchenWebsite---Angular` contains a double-dash (`---`) that looks like a typo
and appears unprofessional on GitHub, npm, and in any URLs or documentation that reference it.

## Suggested Names

| Name | Why |
|------|-----|
| `cloud-kitchen-angular` | Matches the internal project name `cloudkitchenweb` and describes the food-delivery focus |
| `kitchen-website-angular` | Generic, clear, and conventional kebab-case |
| `benito-kitchen-angular` | Personal brand — matches the Netlify URL `benitoinhiskitchen.netlify.app` |

**Recommendation:** `cloud-kitchen-angular` — it matches what the app actually is (a cloud/online
kitchen ordering site) and is consistent with the `cloudkitchenweb` name already in `package.json`.

## How to Rename on GitHub

1. Go to your repository on GitHub.
2. Click **Settings** (top tab row).
3. Under **General → Repository name**, clear the current name and type your new name.
4. Click **Rename**.

## Update Your Local Remote

After renaming on GitHub, run this once in your terminal:

```bash
git remote set-url origin https://github.com/Engr-BenitoIshimwe/cloud-kitchen-angular.git
```

Verify it worked:

```bash
git remote -v
```

> Note: GitHub automatically redirects the old URL for a while, but updating the remote
> immediately avoids confusion.
