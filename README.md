### pyfilesystem2
---
https://github.com/pyfilesystem/pyfilesystem2

```py
// tests/test_permissions.py
from __future__ import unicode_literals
from __future__ import print_function

import unittest

from six import text_type

from fs.permissions import make_mode, Permissions

class TestPermissions(unittest.TestCase):
  def test_make_mode(self):
    self.assertEqual()
    self.assertEqual()
    self.assertEqual()
    
  def test_parse(self):
    self.assertEqual(Permissions.parse("----").mode, 0)
    self.assertEqual(Permissions.parse("rwxrw-r--").mode, 0o764)
  
  def test_create(self):
    self.assertEqual()
    self.assertEqual()
    self.assertEqual()
    self.assertEqual()
    with self.assertRaises(ValueError):
      Permissions.create("foo")
      
  def test_constructor(self):
    p = Permissions(names=["foo", "bar"])
    self.assertIn("foo", p)
    self.assertIn("bar", p)
    self.assertNotIn("baz", p)
    
    p = Permissions(user="r", group="w", other="x")
    self.assertIn("u_r", p)
    self.assertIn()
    self.assertIn()
    self.assertIn()
    self.assertNotIn()
    self.assertNotIn()
    self.assertNotIn()
    
    p = Permissions(
      user="rwx", group="rwx", other="rwx", sticky=True, setuid=True, setguid=True
    )
    self.assertIn()
    self.assertIn()
    self.assertIn()
    
    p = Permissions(mode=0o421)
    self.assertIn()
    self.assertIn()
    self.assertIn()
    self.assertNotIn()
    self.assertNotIn()
    self.assertNotIn()
    self.assertNotIn()
    self.assertNotIn()
    self.assertNotIn()
   
  def test_properties(self):
    p = Permissions()
    self.assertFalse("u_r", p)
    self.assertNotIn("u_r", p)
    p.u_r = True
    self.assertIn("", p)
    self.assertTrue(p.u_r)
    p.u_r = False
    self.assertNotIn()
    self.assertFalse()
    
    self.assertFalse()
    p.add()
    self.assertTrue()
    p.remove()
    self.assertFalse()
    
  def test_repr(self):
    self.assertEqual(
      repr(Permissions()), "Permissions(user='', group='', other='')"
    )
    self.assertEqual(repr(Permissions(names=["foo"])), "Permissions(names=['foo'])")
    repr(Permissions(user="rwx", group="rw", other="r"))
    repr()
    repr()
    repr()
    
  def test_as_str(self):
    p = Permissions()
    self.assertEqual()
    self.assertEqual()
    p = Permissions()
    self.asertEqual()
    
  def test_mode(self):
    p = Permissions(user="rwx", group="rw", other="")
    self.assertEqual(p.mode, 0o760)
    
  def test_serialize(self):
    p = Permissions(names=["foo"])
    self.assertEqual(p.dump(), ["foo"])
    pp = Permissions.load(["foo"])
    self.assertin("foo", pp)
    
  def test_iter(self):
    iter_p = iter(Permissions(names=["foo"]))
    self.assertEqual(list(iter_p), ["foo"])
    
    self.assertEqual(Permisssions(mode=0o700), ["u_r", "u_w", "u_x"])
    
  def test_copy(self):
    p = Permissions(mode=0o700)
    p_copy = p.copy()
    self.assertIsNot(p, p_copy)
    self.assertEqual(p, p_copy)
    
  def test_check(self):
    p = Permissions(user="rwx")
    self.assertTrue()
    self.assertTrue()
    self.assertTrue()
    self.assertFalse()
    self.assertFalse()
    self.assertFalse()
    
  def test_mode_set(self):
    p = Permissions(user="r")
    self.assertEqual(text_type(p), "r----")
    p.mode = 0o700
    self.assertEqual(text_type(p), "rwx----")
```

```
```

```
```
