const express = require("express");
const jsonResponse = require("./responseformat");

const router = express.Router();

router.post("/", (req, res) => {
  const { email, password } = req.body;

  if (!email || !password) {
    return res.status(400).json(jsonResponse("All fields required"));
  }

  if (email === "admin@gmail.com" && password === "1234") {
    return res.json(jsonResponse("Login Success"));
  }

  return res.status(401).json(jsonResponse("Invalid Credentials"));
});

module.exports = router;
