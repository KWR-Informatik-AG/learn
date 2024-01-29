# Cheatsheets

## Essentielles

```bash title="bash/console"
# Stage changes
git add $PATH #(1)!

# Commit changes
git commit -m "$MSG" #(2)!

# Push to origin
git push #(3)!

# Pull from origin
git pull #(4)!
```

1. Bei **`$PATH`** kann es sich sowohl um **Dateien**, als auch um **Ordner** handeln. Im Falle von Ordnern werden alle *Subdateien und Subordner* ebenfalls *rekursiv* hinzugefügt.
2. **`$MSG`** ist die **Commit Beschreibung**. Diese ist ***erforderlich***, um einen Commit zu tätigen.
3. `git push` lädt alle Änderungen zum **Remote/Origin** hoch.
4. `git push` lädt alle Änderungen vom **Remote/Origin** runter.
